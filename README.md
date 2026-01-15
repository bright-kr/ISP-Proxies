# Bright Data ISP Proxies

[![Promo](https://github.com/bright-kr/ISP-Proxies/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.co.kr/proxy-types/isp-proxies?promo=github15)

## Overview
ISP로부터 직접 소싱된 IP로 안전하고 안정적이며 고속의 데이터 수집을 위해 Bright Data의 광범위한 [ISP proxy network](https://brightdata.co.kr/proxy-types/isp-proxies)를 활용하십시오.

- **700,000+ ISP IPs**
- 장기적인 안정성을 갖춘 **Static Residential IPs**
- **99.9% success rate**
- **HTTP(S) & SOCKS5 support**
- **Free Country-Level Targeting**

## Key Features
- **Global Reach**: [multiple countries](https://brightdata.co.kr/locations)에 걸쳐 ISP IPs에 액세스합니다.
- **High Success Rates**: 웹사이트 액세스에서 최대 99.9%의 성공률을 제공합니다.
- **Fast and Stable**: 낮은 지연 시간과 99.99% 네트워크 가용성으로 신뢰할 수 있는 업타임을 제공합니다.
- **Exclusive IP Access**: 일관된 연결을 위한 전용 IPs를 제공합니다.
- **Ethically Sourced**: 모든 ISP proxies는 ISP로부터 직접 제공되며 GDPR 및 CCPA를 준수합니다.

## Pricing Plans
- **Pay As You Go**: 월간 약정 없이 사용 시 $15/GB.
- **Monthly Subscriptions - Shared**:
  - **10 IPs**: $1.80/IP, $18/month + VAT.
  - **100 IPs**: $1.45/IP, $145/month + VAT.
  - **500 IPs**: $1.40/IP, $700/month + VAT.
  - **1,000 IPs**: $1.30/IP, $1300/month + VAT.
  - **Enterprise Plans**: 대규모 데이터 수집 요구에 맞춘 맞춤형 솔루션입니다.
 
- **Monthly Subscriptions - Dedicated**:
  - **10 IPs**: $3.50/IP, $35/month + VAT.
  - **100 IPs**: $2.75/IP, $275/month + VAT.
  - **500 IPs**: $2.60/IP, $1300/month + VAT.
  - **1,000 IPs**: $2.50/IP, $2500/month + VAT.
  - **Enterprise Plans**: 대규모 데이터 수집 요구에 맞춘 맞춤형 솔루션입니다.
 
- **Monthly Subscriptions - Pay/GB**:
  - $12.75/GB, $499/month + VAT.
  - $11.25/GB, $999/month + VAT.
  - $10.50/GB, $1999/month + VAT.
  - **Enterprise Plans**: 대규모 데이터 수집 요구에 맞춘 맞춤형 솔루션입니다.


가입하고 첫 입금 금액에 대해 달러 기준 1:1 매칭을 받으십시오(최대 $500)!

## Getting Started with ISP Proxies
1. **Start Free Trial**: 신용카드가 필요하지 않습니다.
2. **Integration**: Bright Data의 Control Panel 또는 API를 통해 IPs 및 구성을 관리합니다.
3. **Supported Languages**: Python, Java, C#, Node.js 및 Shell에 대한 빠른 시작 가이드가 제공됩니다.

## Code Examples

### Python

```python
import sys

# Replace '[your customerID]', 'isp', and '[your password]' with your actual Bright Data customer ID, zone, and password
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        HttpHost proxy = new HttpHost("brd.superproxy.io", 22225);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-isp", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:22225");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-isp", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
})
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell

```shell
# Replace '[your customerID]' and '[your password]' with your actual credentials
curl --proxy brd.superproxy.io:22225 --proxy-user brd-customer-[your customerID]-zone-isp:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## Integrations
당사의 ISP proxies는 다음을 포함한 널리 사용되는 자동화 도구와 호환됩니다:

- [**Puppeteer**](https://brightdata.co.kr/integration/puppeteer)
- [**Selenium**](https://brightdata.co.kr/integration/selenium)
- [**Playwright**](https://brightdata.co.kr/integration/playwright)
- [**AdsPower**](https://brightdata.co.kr/integration/adspower)
- [**MultiLogin**](https://brightdata.co.kr/integration/multilogin)

## Use Cases
ISP proxies의 일반적인 적용 사례는 다음과 같습니다:

- [**eCommerce**](https://brightdata.co.kr/use-cases/ecommerce): 가격 및 제품 가용성을 추적합니다.
- [**Social Media**](https://brightdata.co.kr/use-cases/social-media-for-marketing): 트렌드와 참여도를 모니터링합니다.
- [**Real Estate**](https://brightdata.co.kr/use-cases/real-estate): 부동산 매물 목록에 대한 데이터를 수집합니다.
- [**Travel**](https://brightdata.co.kr/use-cases/travel): 지역별 여행 딜을 비교합니다.

## FAQ

### What is an ISP Proxy?
ISP proxies는 서버에 할당된 static residential IPs로, 일반적인 residential IP를 사용하는 것처럼 콘텐츠에 액세스할 수 있으면서 더 높은 속도와 안정성을 제공합니다.

### How do ISP Proxies work?
ISP proxies는 ISP로부터 직접 제공되는 IPs를 사용하여, 데이터센터 연결 속도를 유지하면서도 레ジデンシャル 관점에서 콘텐츠에 빠르고 안정적으로 액세스할 수 있게 합니다.

### What are the benefits of using ISP Proxies?
ISP proxies는 [residential IPs](https://brightdata.co.kr/proxy-types/residential-proxies)의 안정성과 익명성에 더해 데이터센터 IPs의 속도를 제공하므로, Web스크레이핑, 광고 검증, SEO 모니터링과 같은 작업에 적합합니다.

### How are ISP Proxies used by businesses?
ISP proxies는 제한된 콘텐츠에 대한 액세스, 광고 검증, 경쟁사 사이트 모니터링, 품질 보증 테스트와 같은 작업에 널리 사용됩니다.

### Are Bright Data's ISP Proxies compliant?
예, 모든 ISP proxies는 윤리적으로 소싱되며 GDPR 및 CCPA를 포함한 데이터 보호 법률을 준수하여 책임 있는 데이터 관행을 보장합니다.