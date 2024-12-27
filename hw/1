import { Application } from "https://deno.land/x/oak/mod.ts";

const app = new Application();

app.use((ctx) => 
{
    // ctx.response.status = 404
    console.log('url=', ctx.request.url)
    let pathname = ctx.request.url.pathname

    ctx.response.body=
    `<html>
        <body>
            <h1>自我介紹</h1>

            <ol>
                <ui><a href="/name">姓名</a></ui>
                <ui><a href="/nationality">國籍</a></ui>
                <ui><a href="/gender">性別</a></ui>
                 <ui><a href="/favfood">最喜歡的食物</a></ui>
            </ol>
        </body>
    </html>`
    
    if (pathname == '/name')
    {
        ctx.response.body = '胡眉真'
    } 
    else if (pathname == '/nationality')
    {
        ctx.response.body = 'Indonesia'
    }
    else if (pathname == '/gender')
    {
        ctx.response.body = "女"
    }  
    else if (pathname == '/favfood')
    {
        ctx.response.body = "takoyaki"
    }
    
    // ctx.response.body = 'Not Found!'

    
});

console.log('start at : http://127.0.0.1:8000')
await app.listen({ port: 8000 })
