# firstCode
my first project
1.常用
获取URL中的参数
const getUrlQuery = function () {
    const resultMap = {}
    let urlQuery = location.search
    if (urlQuery && urlQuery[0] === '?') {
      urlQuery = urlQuery.substring(1).split('&')
      if (urlQuery && urlQuery.length) {
        urlQuery.forEach(function (item) {
          const tmp = item.split('=')
          resultMap[tmp[0]] = tmp[1]
        })
      }
    }
    return resultMap
  }
  const queryStr = getUrlQuery().name
  console.log("链接中的参数", queryStr)
