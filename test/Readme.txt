Ĭ������:
	1.  ��Դģʽ������
	2.  Z/Y/X������
	3.  ��ͨ�˲�ģʽ: һ��ģʽ(����), ��ֹ����
	4.  ��ͨ�˲���ֹƵ��: 51.4HZ
	5.  ���������շ�׼��״̬��INT2
	6.  BDUΪ1 (������ݲ�����, ֱ��MSB��LSB����)
	7.  �����ڴ�Ŀ¼, ����ģʽ
	8.  ����FIFO, FIFO Bypassģʽ
	11. ����RateΪ760��BandwidthΪ50
	12. ����RangeΪ2000DPS
	
���ú�:
	���� #include "l3gd20.h"
	��Щ���ֵ��Ϊ����
	
	L3G_GET_PATH()				�õ�ĳ���ӿڵ�·���� ��ֵΪ·���ַ���
								L3G_GET_PATH(reg):	/sys/devices/virtual/input/input1/reg
	
	L3G_RATE_95HZ				���Ƶ��95HZ
	L3G_RATE_190HZ				���Ƶ��190HZ
	L3G_RATE_380HZ				���Ƶ��380HZ
	L3G_RATE_760HZ				���Ƶ��760HZ
	
	L3G_BANDWTH_0				����0	(��Rateһ��ʹ��ȷ��cutoff��ֵ�� ������ʹ��)
	L3G_BANDWTH_1				����1
	L3G_BANDWTH_2				����2
	L3G_BANDWTH_3				����3
	
	L3G_RATE_95HZ_BANDWTH_12_5	���Ƶ��95HZ, cutoffΪ12.5
	L3G_RATE_95HZ_BANDWTH_25	���Ƶ��95HZ, cutoffΪ25
	L3G_RATE_95HZ_BANDWTH_25	���Ƶ��95HZ, cutoffΪ25
	L3G_RATE_95HZ_BANDWTH_25	���Ƶ��95HZ, cutoffΪ25

	L3G_RATE_190HZ_BANDWTH_12_5	���Ƶ��190HZ, cutoffΪ12.5
	L3G_RATE_190HZ_BANDWTH_25	���Ƶ��190HZ, cutoffΪ25
	L3G_RATE_190HZ_BANDWTH_50	���Ƶ��190HZ, cutoffΪ50
	L3G_RATE_190HZ_BANDWTH_70	���Ƶ��190HZ, cutoffΪ70

	L3G_RATE_380HZ_BANDWTH_20	���Ƶ��380HZ, cutoffΪ20
	L3G_RATE_380HZ_BANDWTH_25	���Ƶ��380HZ, cutoffΪ25
	L3G_RATE_380HZ_BANDWTH_50	���Ƶ��380HZ, cutoffΪ50
	L3G_RATE_380HZ_BANDWTH_100	���Ƶ��380HZ, cutoffΪ100

	L3G_RATE_760HZ_BANDWTH_30	���Ƶ��760HZ, cutoffΪ30
	L3G_RATE_760HZ_BANDWTH_35	���Ƶ��760HZ, cutoffΪ35
	L3G_RATE_760HZ_BANDWTH_50	���Ƶ��760HZ, cutoffΪ50
	L3G_RATE_760HZ_BANDWTH_100	���Ƶ��760HZ, cutoffΪ100
	
	L3G_POWER_DOWN				�رյ�Դ
	L3G_POWER_NORMAL			һ��ģʽ(��X/Y/ZģʽΪdisableʱ�� Ϊ����ģʽ)

	L3G_ZYX_AXIS_DIS			�ر�X/Y/Z��
	L3G_ZYX_AXIS_EN				����X/Y/Z��

	L3G_HIGHPASS_RESET_NORMAL	��ͨ�˲�һ��ģʽ(����)
	L3G_HIGHPASS_REF			��ͨ�˲��ο��˲��ź�ģʽ
	L3G_HIGHPASS_NORMAL			��ͨ�˲���ͨģʽ
	L3G_HIGHPASS_AUTORESET		��ͨ�˲��ж��¼��Զ�����
	
	L3G_HIGHPASS_CUTOFF_0		��ͨ�˲���ֹƵ��ѡ��0, ��Rateһ��ȷ����ֹƵ��(see l3gd20.h)
	L3G_HIGHPASS_CUTOFF_1		
	L3G_HIGHPASS_CUTOFF_2		
	L3G_HIGHPASS_CUTOFF_3		
	L3G_HIGHPASS_CUTOFF_4		
	L3G_HIGHPASS_CUTOFF_5		
	L3G_HIGHPASS_CUTOFF_6		
	L3G_HIGHPASS_CUTOFF_7		
	L3G_HIGHPASS_CUTOFF_8		
	L3G_HIGHPASS_CUTOFF_9		
	
	L3G_BDU_CONTN_UPDATA		�����ݸ���: ��������
	L3G_BDU_NOT_UPDATE			�����ݸ���: ����Ĵ���������

	L3G_RANGE_250DPS			��Χѡ��:	250DPS
	L3G_RANGE_500DPS			��Χѡ��:	500DPS
	L3G_RANGE_2000DPS			��Χѡ��:	2000DPS
	L3G_RANGE_2000DPS			��Χѡ��:	2000DPS

	L3G_FIFO_DIS				FIFO����
	L3G_FIFO_EN					FIFOʹ��

	L3G_HIGHPASS_DIS			��ͨ�˲���ֹ
	L3G_HIGHPASS_EN				��ͨ�˲�ʹ��

	L3G_STATUS_NOT_HAVE			X/Y/Zû���������  (������zyxor, zor, yor, xor�ӿ�ʱ)
								X/Y/Zû�п��õ�����(������zyxda, zda, yda, xda�ӿ�ʱ)
	L3G_STATUS_HAVE				X/Y/Z���������    (������zyxor, zor, yor, xor�ӿ�ʱ)
								X/Y/Z�п��õ�����  (������zyxda, zda, yda, xda�ӿ�ʱ)

	L3G_FIFO_MODE_BYPASS		FIFOģʽ: Bypass mode
	L3G_FIFO_MODE_FIFO			FIFOģʽ: FIFO mode
	L3G_FIFO_MODE_STREAM		FIFOģʽ: Stream mode
	L3G_FIFO_MODE_STREAM_FIFO	FIFOģʽ: Stream-to-FIFO mode
	L3G_FIFO_MODE_BYPASS_STREAM	FIFOģʽ: Bypass-to-Stream mode

	L3G_FIFO_STATUS_NOT_HAVA	FIFO������WTM��, FIFOδ��ȫ���,   FIFO�ǿգ�ʱʹ�ô˺�
	L3G_FIFO_STATUS_HAVE		FIFO�����ڵ���WTM��, FIFO��ȫ���, FIFOΪ�գ�ʱʹ�ô˺�
	
�����ӿ�:
	reg:				�Ĵ����ӿ�, �ɲ鿴�Ĵ�����ֵ���޸ļĴ�����ֵ
						���������ʽ: "0x%02x:0x%02x" 				(����: "0x02:0xef")
						read(L3G_GET_PATH(reg), buf, 100);			��ȡȫ���Ĵ�����ֵ
																	����ֵ֮���Կո�ָ�(ע��: buf����̫С)
						write(L3G_GET_PATH(reg), "0x02:0xef", 10);	�޸ļĴ���0x02ֵΪ0xef 
			
	gyro:				����������ֵ
						�����ʽ: "%d %d %d"						(����: "12 -11 123")
						read(L3G_GET_PATH(gyro), buf, 10);			��ȡ����������ֵ, �����ֵΪ�ַ�������
	
	delay:				�ӳٽӿ�				
						���������ʽ: "%d"							(����: "50")
						read(L3G_GET_PATH(delay), buf, 5);			��ȡֵ
						write(L3G_GET_PATH(reg), "12", 3);			�޸�ֵΪ12	
						
	enable				�����ǵ�Դ����
						���������ʽ: "%d", �������ֵΪ(0-1)
						0: �ϵ�, 1: ����
						
	position			δ֪
	axis				����/����X/Y/Z��
						���������ʽ�� "%d", �������ֵΪ(0-6)
						0: X/Y/Zȫ����ֹ, 1: X��ʹ��, 2: Y��ʹ��, 6: Z��ʹ�� (����ʹ�û�����)
						
	range				��ȡ/��������ѡ��
						���������ʽ�� "%d", �������ֵΪ(250DPS, 500DPS, 2000DPS)
						
	sample				��ȡ/���������������
						���������ʽ: "%d", �������ֵΪ(95HZ, 190HZ, 380HZ, 760HZ)
						
	bandwth				��ȡ/���ò���ѡ��
						���������ʽ�� "%d", �������ֵΪ(0-3) 
						bandwth��Ҫ��rateһͬʹ�ã� ��������odr��cutoff
						rate		bandwth		odr		cutoff
						00 			00 			95 		12.5
						00 			01 			95 		25
						00 			10 			95 		25
						00 			11 			95 		25
						01 			00 			190 	12.5
						01 			01 			190 	25
						01 			10 			190 	50
						01 			11 			190 	70
						10 			00 			380 	20
						10 			01 			380 	25
						10 			10 			380 	50
						10 			11 			380 	100
						11 			00 			760 	30
						11 			01 			760 	35
						11 			10 			760 	50
						11 			11 			760 	100
	
	highpass_mode		��ȡ/���ø�ͨ�˲�ģʽѡ��
						���������ʽ: "%d",  �������ֵΪ(0-3) 
						0: һ��ģʽ(����), 1: �ο��˲��ź�, 2: ��ͨģʽ, 3: �ж��¼��Զ�����
						
	highpass_cutoff_fre	��ȡ/���ø�ͨ�˲���ֹƵ��ѡ��
						���������ʽ: "%d", �������ֵΪ(0-9)
						������ֵ�� ��rateһͬ����
						config		odr=95HZ	odr=190HZ	odr=380HZ	odr=760HZ
						0000 		7.2 		13.5 		27 			51.4
						0001 		3.5 		7.2 		13.5 		27
						0010 		1.8 		3.5 		7.2 		13.5
						0011 		0.9 		1.8 		3.5 		7.2
						0100 		0.45 		0.9 		1.8 		3.5
						0101 		0.18 		0.45 		0.9 		1.8
						0110 		0.09 		0.18 		0.45 		0.9
						0111 		0.045 		0.09 		0.18 		0.45
						1000 		0.018 		0.045 		0.09 		0.18
						1001 		0.009 		0.018 		0.045 		0.09
	
	bdu					��ȡ/���ÿ����ݸ���
						���������ʽ: "%d",  �������ֵΪ(0-1)
						0�� ��������, 1: ����Ĵ���������
						
	temp				��ȡ�¶�ֵ
						�����ʽ: "%d"
	
	hpen				���/���ø�ͨ�˲�ʹ��
						���������ʽ: "%d",  �������ֵΪ(0-1)
						0: ��ֹ, 1: ʹ��
						
	fifo_en				���/����FIFOʹ��
						���������ʽ: "%d",  �������ֵΪ(0-1)
						0: ��ֹ, 1: ʹ��
						
	zyxor				��ȡX/Y/Z�������Ƿ����
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û���������, 1: ���
	
	zor					��ȡZ�������Ƿ����
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û���������, 1: ���
	
	yor					��ȡY�������Ƿ����
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û���������, 1: ���
						
	xor					��ȡX�������Ƿ����
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û���������, 1: ���
						
	zyxda				��ȡX/Y/Z�������Ƿ��������ݿ���
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û�п�������, 1: ��
						
	zda					��ȡZ�������Ƿ��������ݿ���
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û�п�������, 1: ��
						
	yda					��ȡY�������Ƿ��������ݿ���
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û�п�������, 1: ��
						
	xda					��ȡX�������Ƿ��������ݿ���
						�����ʽ: "%d",  ���ֵΪ(0-1)
						0: û�п�������, 1: ��
						
	fifomode			��ȡ/����FIFOģʽ
						���������ʽ: "%d", �������ֵΪ(0-4)
						0: Bypass mode, 1: FIFO mode, 2: Stream mode
						3: Stream-to-FIFO mode, 4: Bypass-to-Stream mode
						
	watermk				��ȡ/����FIFOˮλ�ȼ�
						���������ʽ: "%d"
						
	watermk_status		��ȡˮλ�ȼ���״̬
						�����ʽ: "%d", ���ֵΪ(0-1)
						0: FIFO������WTM��, 1: FIFO�����ڵ���WTM��
						
	fifoovrn			��ȡFIFO�Ƿ����
						�����ʽ: "%d", ���ֵΪ(0-1)
						0: FIFOδ��ȫ���, 1: FIFO��ȫ���
						
	fifoempty			��ȡFIFO�Ƿ�Ϊ��
						�����ʽ: "%d", ���ֵΪ(0-1)
						0: FIFO����, 1: FIFOΪ��
						
	fifolevel			��ȡFIFO�洢�����ݵȼ�
						�����ʽ: "%d"