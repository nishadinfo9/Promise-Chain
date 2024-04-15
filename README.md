# Promise-Chain


function getDeta(data) {
    return new Promise((reselve, reject)=>{
        setTimeout(() => {
            console.log('data = ' + data);
            reselve("success")
        }, 100);
    })
}


getDeta(1)
    .then((res)=>{
        return getDeta(2)
        })
    .then((res)=>{
        return getDeta(3)
        })
    .then((res)=>{
        return getDeta(4)
        })
    .then((res)=>{
        return getDeta(5)
        })
    .then((res)=>{
        console.log(res);
        })
