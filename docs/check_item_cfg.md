# check item������
edwin��û�е�adminҳ�����ṩcheck item������, ���������Ȥ�Ļ�, ��ӭΪedwin�ṩһ��adminģ��. ��û��adminģ��֮ǰ, ���ǲ��ò�ֱ����DB��������Ӧ�ı�, ���õ���, ��ʵ�ǳ���. 

## 1. team������ 
��EDWIN_TEAM_CFG��, ��������team�Ļ�����Ϣ. �ֶ��嵥����: 

| �ֶ�        | ����   |  ��ע  |
| --------   |  :-----  | :----  |
| OWNER_TEAM_CODE| Team�ı��� |       |
| EMAIL_TO_LIST| Team�������б�     |���Ƕ������ţ���Ӣ�Ķ��Ż�ֺŷָ�  |
| SMS_MAIL_TO| Team�Ķ��Ÿ澯��Ӧ������� |   |
| SMS_MAIL_TITLE| Team�Ķ��Ÿ澯��Ӧ���������       |   |
| PHONE_MAIL_TO|  Team�ĵ绰�澯��Ӧ�������    |   |
| PHONE_MAIL_TITLE|Team�ĵ绰�澯��Ӧ���������   |  |


## 2. check item������ 
�ڱ�EDWIN_CHECK_ITM_CFG�����ü����Ŀ. �ֶ��嵥����:  

| �ֶ�        | ����   |  ��ע  |
| --------   |  :-----  | :----  |
|ITM_CODE|  check item�ı���| ����Ψһ��      |
|ITM_TITLE| check item�ı��� | �������ʾ��webҳ��      |
|ITM_CATEGORY | check item����� |       |
|ENABLED_FLAG| ���ñ�־, YΪ����, NΪ���� |       |
|HOST| ���agent�������ĸ������� | ������Ϊ����Ϣ��������, edwin�������������Զ�����agent  |
|CHECK_SCRIPT| agent�������ϸ·�� | ������Ϊ����Ϣ��������, edwin�������������Զ�����agent      |
|CHECK_INTERVAL_MINUTE| agent�����ִ��Ƶ�� | edwin�����������ֵ���ж����agent�Ƿ���δ����      |
|CHECK_VALUE_IS_NUMBER| ������Ƿ��������, YΪ������, NΪ�������� |       |
|DESCRIPTION  | check item��˵�� |       |
|OWNER_TEAM_LIST| �����team code  |����Ƕ��team��ͬ����, ��Ӣ�Ķ��Ż�ֺŷָ�team code       |
|WARNING_LIMIT| ���漶����ֵ | ���ڼ������������check item, �����趨��ֵ      |
|CRITICAL_LIMIT| ����������ֵ | ���ڼ������������check item, �����趨��ֵ     |
|SHADOW_DATA| Ӱ�� Data, ��ֵ������ļ����һ�𱣴浽EDWIN_CHECK_ITM_LOG���� |�ܸ߶˵�����Ŷ, ����ϸ��|
|WARNING_MAIL_CC| ���漶�쳣�᳭�ͽo˭ |       |
|CRITICAL_MAIL_CC| �������쳣�᳭�ͽo˭ |       |
|CRITICAL_SMS_FLAG| ���ڽ������쳣, �Ƿ������Ͷ��Ÿ澯 |       |
|CRITICAL_CALL_FLAG| ���ڽ������쳣, �Ƿ�����绰�澯  |       |
|ALLOW_REPEATED_SMS_ALARM| �Ƿ������ظ����ű��� |       |   
|ALLOW_REPEATED_CALL_ALARM| �Ƿ������ظ��绰���� |       |  
|ALLOW_REPEATED_MAIL_ALARM | �Ƿ������ظ��ʼ����� |       |

**SHADOW_DATA** �ĸ߼��÷�   

����˵����, ����������Ҫ���windows����C�̺�D�̵�ʹ�����, �ٶ��������������ֱ���, C�̴���70%ʹ����, D��80%��ʹ����. ��������������:  

1. �ֱ�C�̺�D�����ò�ͬ��check item, ��Ȼ��Ӧ����Ҫ����agent����. ����Ȼ, ����agent������뼸��һģһ��, д��������һģһ���ĳ���, �Ⲣ���Ǻõ�����. ����, ����һ��Ļ�, ��������������, ���ǵ�check item�ᱩ��, ��������Ҳ�ܲ���.  

2. ��һ���Ƽ���������, ����һ��check item��֧�������̵ļ��, �����������̵ļ���ֵ��ͬ, ��α�д���agent��? �ܼ�, ����ΪSHADOW_DATA����һЩָ��, ���� "C_disk_critical=0.70 || C_disk_critical=0.80",  ��agent������,����ͨ��api��ȡ�����ָ��, ��������, �õ�C�̺�D�̸����趨�ļ���ֵ, ���ռ���ֵ���ʵ�ʵĴ���ʹ��������. 

## 3. չ��ҳ������� 
֮ǰ���ܹ�, edwin���ڼ�������֯��ʽ, ��С������: check item -> pagelet -> page -> dashboard, ����page��edwin��һ������չ��ҳ��, һ��չ��ҳ�������� pagelet(��������), һ����������԰������check item. ����, edwin�ṩһ��dashboard�̶�չ��ҳ, �Զ���������չ��ҳ�ļ�ؽ��.  

edwin����֧�ֶ��team, Ϊ�˷������team���, ����Ȼ�ؿ���Ϊ��ͬ��team���ò�ͬ��pageҳ.  

��ʵ�ʵ�ʵʩ��, ������������һ������, ͬһ��server���ܺü���team����, �������server�ļ��, �⼸��team���ܶ��ܹ���.edwin ���Ժ����ɽ�����ֽ����ע����. ��Ϊ, ��edwin��һ��check item ���Գ����ڶ��������(pagelet)��, Ҳ����ζ��, һ��check item���Գ����ڶ��չ��ҳ��, ��������, ����ô��. 

### 3.1 pageҳ������
��EDWIN_PAGE��, ��������page����, �ֶ��嵥����: 

| �ֶ�        | ����   |  ��ע  |
| --------   |  :-----  | :----  |
|PAGE_CODE | pageҳ�ı���| ����     |
|PAGE_TITLE| pageҳ��web�ϵ���ʾ����|      |
|DISPLAY_FLAG|�Ƿ�Ҫ��web����ʾ | YΪ��ʾ, NΪ����ʾ     |
|DESCRIPTION|| ��pageҳ������     |


### 3.2 ������(pagelet)������ 
��EDWIN_PAGELET��, ��������page����, �ֶ��嵥����: 

| �ֶ�        | ����   |  ��ע  |
| --------   |  :-----  | :----  |
|PAGELET_CODE|pagelet�ı���| ����     |
|PAGELET_TITLE|pagelet��web�ϵ���ʾ����|      |
|PAGE_CODE|������page����|      |
|DISPLAY_ORDER|��page�ϵ���ʾ����| ���ԽСԽ��ǰ��ʾ     |
|DISPLAY_FLAG|�Ƿ�Ҫ��page����ʾ|  YΪ��ʾ, NΪ����ʾ     |
|DESCRIPTION|��pagelet������|      |     


### 3.3 ������(pagelet)��Ҫ��ʾ��Щcheck item
�ڱ�EDWIN_PAGELET_CHECK_LIST, ������ĳ��������Ҫ��ʾ��Щcheck item��, ���嵥����:  
 
| �ֶ�        | ����   |  ��ע  |
| --------   |  :-----  | :----  |
|PAGELET_CODE| pagelet�ı���|      |
|CHECK_ITM_CODE|�������ĸ�check item|      |
|DISPLAY_ORDER| check item��pagelet�е���ʾ����| ���ԽСԽ��ǰ��ʾ     |
|DISPLAY_FLAG|�Ƿ�Ҫ��pagelet����ʾ|  YΪ��ʾ, NΪ����ʾ        |



## 3. �������  
��EDWIN_CHECK_ITM_LOG��, �������꾡�ļ����, �ֶ��嵥����:  

| �ֶ�        | ����   |  ��ע  |
| --------   |  :-----  | :----  |
|ITM_CODE| check item�ı���|      |
|CHECK_DATE|�������|      |
|CHECK_TIMESTAMP| ������ϸʱ��|   |
|CHECK_STATUS|���Ľ��, ����/���漶�쳣/�������쳣|     |
|CHECK_VALUE|���ľ�����ֵ| �������ڼ������������check item   |
|CHECK_DETAIL_MSG|��������꾡����, ����webչ��|֧��htmlд��, �����Ҫ��ʾС�ں�, ��Ҫ��htmlת��|
|CHECK_NOTIFICATION_MSG|��������꾡����, �����쳣ʱ���ʼ�֪ͨ|֧��htmlд��, �����Ҫ��ʾС�ں�, ��Ҫ��htmlת�� |
|WARNING_LIMIT|���漶����ֵ| �������ڼ������������check item      |
|CRITICAL_LIMIT|����������ֵ| �������ڼ������������check item      |
|SHADOW_DATA|Ӱ�� Data, ��ֵ��Դ��check item���ñ��SHADOW_DATA�ֶ� |     |
|IS_WARNING_EVENT|�Ƿ��Ǿ��漶�쳣, ȡֵY��N|  |
|IS_CRITICAL_EVENT|�Ƿ��ǽ������쳣, ȡֵY��N|     |
|IS_NEW_WARNING_EVENT|�Ƿ����µľ��漶�쳣, ȡֵY��N|     |
|IS_NEW_CRITICAL_EVENT|�Ƿ����µĽ������쳣, ȡֵY��N|     |
|ALARM_SEND_STATUS|��������״̬| ���쳣�Żᱨ��    |
|ALARM_SEND_BEGIN_TIME|�������͵Ŀ�ʼʱ��|     |
|ALARM_SEND_END_TIME|�������͵Ľ���ʱ��|     |

