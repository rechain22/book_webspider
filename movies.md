# Loggling 的使用
## 设置格式 
logging.basicConfig(level=logging.INFO, format="...")
## 输出内容
logging.info("get detail url %s", detail_url)

# 主要函数总结
## scrape_index()
爬取索引页面（虚函数）
## scrape_detail()
爬取详细页面（虚函数）
## scrape_page()
爬取页面html（实际函数）

## parse_index()
解析索引页面，获取详细页面地址
## parse_detail()
解析详细页面，获取电影信息

## 保存数据 save_data()
### Json 的使用
#### json.dump() 的参数
1. 输出数据
2. open(filename,'w',encoding='utf-8')
3. ensure_ascii=False （保证中文正常）
4. indent=2 

# Multiprocessing
1. 创建进程池 Pool
2. pool.map(被调用函数， 被遍历参数)
3. pool.join() 主进程阻塞后，子进程继续运行。子进程全部运行完，再关闭主进程。（多进程特有的盛名步骤吧）