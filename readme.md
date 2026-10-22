# OCDM radar communication integrated signal fuzzy function [MATLAB code]

\n        \n  
\n        \n  
\n        \n  
\n        \n  
\n        \n      %% Comparison of Fuzzy Functions between OCDM and OFDM\nclear all;close all;clc\n\n\n% Subcarrier number\nN_c=16;\n% Pulse duration\nT_b=1e-6;\n% Normalize time\nx=linspace(-1,1,32*N_c);%-1:0.001:1;\n% Normalize frequency\ny=-5:0.01:5;\n% Frequency adjustment\nmu=16/T_b^2;\n% Symbol Weights\n% w=ones(N_c,1);\nw=chebwin(N_c,50);\n%% Fuzzy Functions\n[X,Y]=meshgrid(x,y);\n[amf,amt]=size(X);\nAF_ofdm = AFmean_single_symbol( N_c,T_b,x,y,w);\nAF_ocdm = AFmean_lfm_OFDM_single( N_c,T_b,mu,x,y,w );\n\n\nfigure;grid on;hold on\nsurf(X,Y,AF_ofdm,'EdgeColor','none')\n% title('OFDM average blur function', 'fontsize', 14)\nxlabel('Normalized latency','fontsize',14),ylabel('Normalization frequency shift','fontsize',14)\ncolormap('default')\n% surface(x, [0,0], [zeros(1,amt);AF_ocdm(1,:)],'EdgeColor',[0 0 0],'FaceColor',[0 0 0]);\nzlim([0,1]);\nview(-46,26)\n\n\n\n\nfigure;grid on;hold on\nsurf(X,Y,AF_ocdm,'EdgeColor','none')\n% title('OFDM average blur function', 'fontsize', 14)\nxlabel('Normalization of latency','fontsize',14),ylabel('Normalization frequency shift','fontsize',14)\ncolormap('default')\n% surface(x, [0,0], [zeros(1,amt);AF_ocdm(1,:)],'EdgeColor',[0 0 0],'FaceColor',[0 0 0]);\nzlim([0,1]);\nview(-46,26)\n% view(0,90)\n%% Distance blur function\nAC_ofdm=AF_ofdm(501,:);\nAC_ocdm=AF_ocdm(501,:);\n\n\nfigure;grid on;hold on;\nplot(x,AC_ofdm,'k','linewidth',1.5) \nplot(x,AC_ocdm,'b','linewidth',1.5) \ntitle('Comparison of distance blur functions','fontsize',14);\nxlabel('Normalized delay','fontsize',14),ylabel('Normalize magnitude','fontsize',14)\nlegend('OFDM','OCDM')\n% ylim([0,1]);\n% xlim([-0.2,0.2])\n%% Speed blur function\nDC_ofdm=AF_ofdm(:,256);\nDC_ocdm=AF_ocdm(:,256);\n\n\nfigure;grid on;hold on;\nplot(y,DC_ofdm,'k','linewidth',1.5) \nplot(y,DC_ocdm,'b','linewidth',1.5) \ntitle('Comparison of Speed Blur Functions','fontsize',14);\nxlabel('Normalization frequency shift','fontsize',14),ylabel('Normalize amplitude','fontsize',14)\nlegend('OFDM','OCDM')\n% xlim([y(1),y(end)]);\n% xlim([-5,5])\n\n  

## Images

![OCDM radar communication integrated signal fuzzy function [MATLAB code]](01.jpg)
![OCDM radar communication integrated signal fuzzy function [MATLAB code]](02.jpg)
![OCDM radar communication integrated signal fuzzy function [MATLAB code]](03.jpg)
![OCDM radar communication integrated signal fuzzy function [MATLAB code]](04.jpg)
![OCDM radar communication integrated signal fuzzy function [MATLAB code]](05.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
