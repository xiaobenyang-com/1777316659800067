# 域名查询服务 Lookup Domain

一个提供全面域名研究工具（包括RDAP、WHOIS和DNS查询功能）的模型上下文协议（MCP）服务器。
A Model Context Protocol (MCP) server that provides comprehensive domain name research tools, including RDAP, WHOIS, and DNS query functionality.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| domain_lookup | Look up domain information using RDAP protocol with WHOIS fallback. Provides comprehensive domain registration details, nameservers, contacts, and status information. |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659800067](https://mcp.xiaobenyang.com/inspector/1777316659800067)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659800067](https://mcp.xiaobenyang.com/inspector/1777316659800067)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "域名查询服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659800067/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "域名查询服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659800067/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "域名查询服务": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659800067",
          },
          "transport": "stdio"
        }
      }
}

```
