import pygame,sys

pygame.init()
white=pygame.image.load('White.png')
White=pygame.display.set_mode((700,700))
#varieble
a1=700
b1=690
a2=690
b2=700
aa1=0
aa2=0
bb1=0
bb2=0
blue=pygame.image.load('Blue.png')
red=pygame.image.load('red.png')
t_image=pygame.image.load('tankpng.parspng.com-12.png')
t_Image=pygame.transform.scale(t_image,(30,30))
Red=pygame.transform.scale(red,(60,60))
Blue=pygame.transform.scale(blue,(60,60))
window=pygame.display.set_mode((700,700))
window.fill((255,255,255))
c=30
d=30
movetank=pygame.image.load('tankpng.parspng.com-12.png')
moveTank=pygame.transform.scale(movetank,(60,60))
x=550
w=550
speed=10.008
moveTank2=moveTank
x2=100
w2=100
white=pygame.image.load('White.png')
White=pygame.transform.scale(white,(1,1))
he=0
we=0
d=-20
tank1_j=0


def kooh(x,w):
    if x<530 and x>60 and w<60 and w>30:

        return(True)

    if x<580 and x>410 and w<275 and w>245:

        return(True)
    if x<230 and x>30 and w<515 and w>485:

        return(True)

    return(False)
def kooh_2(x,w):
    if x<510 and x>60 and w<60 and w>30:

        return(True)

    if x<580 and x>410 and w<275 and w>245:

        return(True)
    if x<230 and x>30 and w<515 and w>485:

        return(True)

    return(False)
def jade(x,w):
            RF=False
            
            
            if x<=350-20 and x>=350-50 and w<=600-5 and w>=410-30:
                tank1_j=1
                RF=False
                return(tank1_j,RF)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=600 and x>=365-20 and w<=600-20 and w>=600-50:
                tank1_j=1
                RF=True
                return(tank1_j,RF)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=350 and x>=125 and w<=400-30 and w>=400-60:
                RF=True
                tank_j=1
                return(tank_j,True)
            else:
                tank1_j=0
                #return(tank1_j)
            #kharab azz inga be paain be jade2 kopi nashode
            if x<=150+25 and x>=150+10 and w<=400 and w>=200:
                RF=False
                tank_j=1
                return(tank1_j,RF)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=600 and x>=150 and w<=200-10 and w>= 200-25:
                RF=True
                tank_j=1
                return(tank1_j,RF)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=600+25 and x>=600+10 and w<=200 and w>=150:
                RF=False
                tank_j=1
                return(tank1_j,RF)
            else:
                tank1_j=0
                #return(tank1_j)
            return(0,False)
        
def jade2(x,w):
            
            RF2=False
            if x<=350-16 and x>=350-30 and w<=600 and w>=400:
                tank1_j=1
                RF2=False
                return(tank1_j,RF2)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=600 and x>=350-20 and w<=600-20 and w>=600-50:
                tank1_j=1
                RF2=True
                return(tank1_j,RF2)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=350 and x>=150 and w<=400-10 and w<=400-25:
                RF2=True
                tank_j=1
                return(tank1_j,RF2)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=150+25 and x>=150+10 and w<=400 and w>=200:
                RF2=False
                tank_j=1
                return(tank1_j,RF2)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=600 and x>=150 and w<=200-10 and w>= 200-25:
                RF2=True
                tank_j=1
                return(tank1_j,RF2)
            else:
                tank1_j=0
                #return(tank1_j)
            if x<=600+25 and x>=600+10 and w<=200 and w>=150:
                RF2=False
                tank_j=1
                return(tank1_j,RF2)
            else:
                tank1_j=0
                #return(tank1_j)
            return(0,False)              
        
def keycontrol():
    for event in pygame.event.get():
        if event.type==pygame.KEYDOWN:        
            if event.key==pygame.K_w:
                   w -= speed
                   window.blit(Red,(x+ 20+d,w+30+d))
            if event.key==pygame.K_s:
                     w += speed
                     window.blit(Red,(x+ 20+d,w+10+d))
            if event.key==pygame.K_a:
                    x-= speed
                    window.blit(Red,(x+ 30+d,w+20+d))
            if event.key==pygame.K_y:
                    w2 -= speed
                    window.blit(Blue,(x2+20+d,w2+30+d))
            if event.key==pygame.K_h:
                    w2 += speed
                    window.blit(Blue,(x2+20+d,w2+10+d))
            if event.key==pygame.K_j:
                    x2 += speed
                    window.blit(Blue,(x2+10+d,w2+20+d))
            if event.key==pygame.K_g:
                    x2 -= speed
                    window.blit(Blue,(x2+30+d,w2+20+d))
            if event.key==pygame.K_d:
                    x += speed
                    window.blit(Red,(x+ 10+d,w+30+d))
            return()





def alfa(x,w,x2,w2):
    he=0
    we=0
    a1=50
    b1=100
    a2=70
    b2=70
    for a in range(700*700):
                                                                                                                                                                                                                                                                                          
        if  (he<= x+15  and he >= he+15+30 and  we<=w+20 and we>=w+20+30) or (he<= x2+15  and he >= x2+15+30 and  we<=w2+20 and we>=w2+20+30) :
            window.blit(White,(he,we))
        he=he+1
        if he>=700:
            we=we+1
            he=0
    window.blit(t_Image,(350,350))
    window.blit(t_Image,(600,20))
    window.blit(t_Image,(100,100))
    window.blit(t_Image,(650,600))
    window.blit(t_Image,(600,400))
    window.blit(t_Image,(10,500))
    window.blit(t_Image,(350,20))
    window.blit(t_Image,(690,690))
    window.blit(t_Image,(15,400))
    window.blit(t_Image,(350,355))
    window.blit(t_Image,(450,450))
    window.blit(t_Image,(200,550))
    window.blit(t_Image,(550,250))
    window.blit(t_Image,(100,300))
    for y in range(15):
        pygame.draw.aaline(window,(1,1,1),(a1,b1),(a2,b2),0)
        pygame.draw.aaline(window,(1,1,1),(a2,b2),(a1+30,b1),0)
        pygame.draw.aaline(window,(1,1,1),(a1+10,b1-15),(a2+5,b2+15),0)
        a2=a2+30
        a1=a1+30
    aa1=40
    bb1=550
    aa2=60
    bb2=520   
    for y in range(7):
        pygame.draw.aaline(window,(1,1,1),(aa1,bb1),(aa2,bb2),0)
        pygame.draw.aaline(window,(1,1,1),(aa2,bb2),(aa1+30,bb1),0)
        pygame.draw.aaline(window,(1,1,1),(aa1+10,bb1-15),(aa2+5,bb2+15),0)
        aa2=aa2+30
        aa1=aa1+30
    aa1=410
    bb1=310
    aa2=aa1+20
    bb2=bb1-30
    for y in range(7):
        pygame.draw.aaline(window,(1,1,1),(aa1,bb1),(aa2,bb2),0)
        pygame.draw.aaline(window,(1,1,1),(aa2,bb2),(aa1+30,bb1),0)
        pygame.draw.aaline(window,(1,1,1),(aa1+10,bb1-15),(aa2+5,bb2+15),0)
        aa2=aa2+30
        aa1=aa1+30
    aa1=600
    bb1=500
    aa2=aa1+20
    bb2=bb1-30  
    for i in range(10):
        for h in range(i+2):
            pygame.draw.aaline(window,(1,1,1),(aa1,bb1),(aa2,bb2),0)
            pygame.draw.aaline(window,(1,1,1),(aa2,bb2),(aa1+30,bb1),0)
            pygame.draw.aaline(window,(1,1,1),(aa1+10,bb1-15),(aa2+5,bb2+15),0)
            aa2=aa2+30
            aa1=aa1+30
        aa1=aa1-10-((i+2)*30)
        bb1=bb1+10+((i+2)*30)
        aa2=aa1+20
        bb2=bb1-30
    pygame.draw.aaline(window,(1,1,1),(350,600),(350,400),0)
    pygame.draw.aaline(window,(1,1,1),(350,600),(600,600),0)
    pygame.draw.aaline(window,(1,1,1),(350,400),(150,400),0)
    pygame.draw.aaline(window,(1,1,1),(150,400),(150,200),0)
    pygame.draw.aaline(window,(1,1,1),(150,200),(600,200),0)
    pygame.draw.aaline(window,(1,1,1),(600,200),(600,150),0)
    Tan=0

    return()


while 3>2:
    kooh1=kooh(x,w)
    kooh2=kooh_2(x2,w2)
    a=alfa(x,w,x2,w2)
    b,RF=jade(x,w)
    c,RF2=jade2(x2,w2)
    window.blit(moveTank,(x,w))
    window.blit(moveTank2,(x2,w2))
    for event in pygame.event.get():
        if event.type== pygame.QUIT:
            pygame.quit()
            sys.exit()
    #keycontrol()
        if kooh1==True:
            if event.type==pygame.KEYDOWN:
                if event.key==pygame.K_a:
                        x-= speed
                        window.blit(Red,(x+ 30+d,w+20+d))

                if event.key==pygame.K_d:
                        x += speed
                        window.blit(Red,(x+ 10+d,w+30+d))
        if kooh2==True:
            if event.type==pygame.KEYDOWN:

                if event.key==pygame.K_j:
                        x2 += speed
                        window.blit(Blue,(x2+10+d,w2+20+d))
                if event.key==pygame.K_g:
                        x2 -= speed
                        window.blit(Blue,(x2+30+d,w2+20+d))
            
            
        
        if b==0 and kooh1==False :
            if event.type==pygame.KEYDOWN:
                if event.key==pygame.K_w:
                       w -= speed
                       window.blit(Red,(x+ 20+d,w+30+d))
                if event.key==pygame.K_s:
                         w += speed
                         window.blit(Red,(x+ 20+d,w+10+d))
                if event.key==pygame.K_a:
                        x-= speed
                        window.blit(Red,(x+ 30+d,w+20+d))

                if event.key==pygame.K_d:
                        x += speed
                        window.blit(Red,(x+ 10+d,w+30+d))
        if c==0 and event.type==pygame.KEYDOWN and kooh2==False:
                if event.key==pygame.K_y:
                        w2 -= speed
                        window.blit(Blue,(x2+20+d,w2+30+d))
                if event.key==pygame.K_h:
                        w2 += speed
                        window.blit(Blue,(x2+20+d,w2+10+d))
                if event.key==pygame.K_j:
                        x2 += speed
                        window.blit(Blue,(x2+10+d,w2+20+d))
                if event.key==pygame.K_g:
                        x2 -= speed
                        window.blit(Blue,(x2+30+d,w2+20+d))
            

        if b==1 and kooh1==False:
                if event.type==pygame.KEYDOWN:
                    if event.key==pygame.K_w and RF==False :
                        for i in range(5):
                           w -= speed
                           window.blit(Red,(x+ 20+d,w+30+d))
                    elif event.key==pygame.K_w and RF!=False:
                           w -= speed
                           window.blit(Red,(x+ 20+d,w+30+d))
                        

                    if event.key==pygame.K_s and RF==False:
                        for i in range(5):
                             w += speed
                             window.blit(Red,(x+ 20+d,w+10+d))
                    elif event.key==pygame.K_s and RF!=False:
                             w += speed
                             window.blit(Red,(x+ 20+d,w+10+d))
                    if event.key==pygame.K_a and RF==True:
                        for i in range(5):
                            x-= speed
                            window.blit(Red,(x+ 30+d,w+20+d))
                    elif event.key==pygame.K_a and RF!=True:
                             x-= speed
                             window.blit(Red,(x+ 30+d,w+20+d))
                    if event.key==pygame.K_d and RF==True:
                        for i in range(5):
                            x += speed
                            window.blit(Red,(x+ 10+d,w+30+d))
                    elif event.key==pygame.K_d and RF!=True:
                            x += speed
                            window.blit(Red,(x+ 10+d,w+30+d))
                        
        if c==1 and event.type==pygame.KEYDOWN and kooh2==False:
                    if event.key==pygame.K_y and RF2==False:
                        for i in range(5):
                            w2 -= speed
                            window.blit(Blue,(x2+20+d,w2+30+d))
                    elif event.key==pygame.K_y:
                            w2 -= speed
                            window.blit(Blue,(x2+20+d,w2+30+d))
                        
                    if event.key==pygame.K_h and RF2==False:
                        for i in range(5):
                            w2 += speed
                            window.blit(Blue,(x2+20+d,w2+10+d))
                    elif event.key==pygame.K_h:
                            w2 += speed
                            window.blit(Blue,(x2+20+d,w2+10+d))
                    if event.key==pygame.K_j:
                        for i in range(5):
                            x2 += speed
                            window.blit(Blue,(x2+10+d,w2+20+d))
                    if event.key==pygame.K_g:
                        for i in range(5):
                            x2 -= speed
                            window.blit(Blue,(x2+30+d,w2+20+d))
                

    
    pygame.display.update()




