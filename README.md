# mysql-c-plus-plus-3.2.3-new
mysql-c-plus-plus-3.2.3-new
lib\query.h 文件新加
	std::string getSQL(){return sbuffer_.str();}
	void open(){sqlinit=sbuffer_.str();}//打开
	void close();//关闭
	std::string sqlinit;//打印sql
lib\query.cpp 文件新加
void
Query::close()
{
	seekp(0);
	clear();
	sbuffer_.str(sqlinit);

	parse_elems_.clear();
	template_defaults.clear();
}
………………
,,,,,,
[[[[]]]]