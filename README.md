# mysql-c-plus-plus-3.2.3-new
mysql-c-plus-plus-3.2.3-new
lib\query.h �ļ��¼�
	std::string getSQL(){return sbuffer_.str();}
	void open(){sqlinit=sbuffer_.str();}//��
	void close();//�ر�
	std::string sqlinit;//��ӡsql
lib\query.cpp �ļ��¼�
void
Query::close()
{
	seekp(0);
	clear();
	sbuffer_.str(sqlinit);

	parse_elems_.clear();
	template_defaults.clear();
}