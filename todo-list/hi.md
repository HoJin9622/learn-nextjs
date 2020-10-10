window, document는 서버 사이드에서는 갖고 있지 않으므로 window/document is not defined 에러를 출력하게 된다.
alert 역시 마찬가지로 window.alert, localstorage도 window.localstorage 이므로 에러가 출력된다.

해결하기위해 useEffect를 사용하여 해결한다.
useEffect의 componentDidMount는 client side가 rendering 된 후에 일어난다.
그렇기 때문에 useEffect에 localstorage, window, document, alert 등을 사용하면 에러없이 동작하게 된다.