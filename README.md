scrapy三种登录

第一种：def start_requests(self)

第二种：yield scrapy.FormRequest(）

第三种：def parse(self, response):

          yield scrapy.FormRequest.from_response(
          
            response, #自动的从response中寻找from表单
            
            formdata={"login":"noobpythoner","password":"zhoudawei123"},
            
            callback = self.after_login
            
           )
