ʹ��Spring Security��
1. ��������Spring Security ��ص�������Ȼ��дһ�������࣬��������̳���WebSecurityConfigurerAdapter�����ڸ�������
������@EnableWebSecurity ע�⿪��WebSecurity��ע��configureGlobal��������configureGlobal��������Ҫ����AuthenticationManagerBu ilder,AuthenticationManagerBuilder �����˶�ȡ�û�����֤��Ϣ�ķ�ʽ�����Դ��ڴ��ж�ȡ��Ҳ���Դ����ݿ��ж�ȡ�������������ķ�ʽ��
	a. �ڴ��ȡ�ο�ʾ��SecurityConfiguration1.java �� SecurityConfiguration2.java
	b. ���ݿ��ȡ�ο�SecurityConfiguration4.java  Ҫ����mysql���ݿ����½�spring security���ݿ⣬Ȼ����resources/scheme.sql��ʼ������


2. ��Ҫ����HttpSecurity, HttpSecurity �������������֤���򣬼���ЩURI ������Ҫ��֤����Щ����Ҫ���Լ���Ҫӵ��ʲôȨ��
���ܷ��ʡ���������Ҫ������������İ�ȫ���ã���Ҫͨ������������@EnableGlobalMethodSecurityע�⿪�������������ϵ�
��ȫ����֧��secureEnabled ��jsr250Enabled ��prePostEnabled ��3�ַ�ʽ���õ�������prePostEnabled �����У� prePostEnabled ����PreAuthorize ��PostAuthorize������ʽ�� һ��ֻ�õ�PreAuthorize ���ַ�ʽ��
	�ڷ�����дȨ��ע������ַ�����
       a. @PreAuthorize("hasRole('ADMIN')")
       b. @PreAuthorize("hasAuthority('ROLE_ADMIN')")  ����д�����
       һ���������Ȩ�޵��д����
       a. @PreAuthorize("hasAnyRole('ADMIN','USER')")
       b. @PreAuthorize("hasAnyAuthority('ROLE_ADMIN','ROLE_USER')")
       
	������������İ�ȫ���òο�ʾ��SecurityConfiguration3.java �� BlogController���delete�����ϵ�preAuthorizeע��

3. �½���ϸ�����Ķ��������SpringCloud��΢����ĵ�13�½� Spring Boot Security��⡣