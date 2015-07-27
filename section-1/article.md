## ~~Very~~ **Extremely** Interesting!

```
      protected void Page_Load(object sender, EventArgs e)
      {
           string path = Request.Path;
           path = path.Substring(1);
           string jsonResponse = string.Empty;

           switch (path)
           {
               case CustomApiTest.TEST_START_TRACE_ROUTE:
                    jsonResponse = StartTrace();
                    break;
               default:
                    Response.StatusCode = 404;
                    return;
           }

           Response.Clear();
           Response.ContentType = "application/json; charset=utf-8";
           Response.Write(jsonResponse);
           Response.End();
      }
```

[🏠](../README.md)
