* `比较两个对象是否完全相同`

        function deepEqual(obj1, obj2) {
            if (obj1 === obj2) {
                return true;
            }
            if (typeof obj1 !== 'object' || typeof obj2 !== 'object' || obj1 === null || obj2 === null) {
                return false;
            }
            const keys1 = Object.keys(obj1);
            const keys2 = Object.keys(obj2);
            if (keys1.length !== keys2.length) {
                return false;
            }
            for (let key of keys1) {
                if (!keys2.includes(key) || !deepEqual(obj1[key], obj2[key])) {
                    return false;
                }
            }
            return true;
        }
  
* `将一个对象的value复制出来作为一个新的数组，并把他的key作为value数组里的id`
* eg. 34543645-xxxx123213-xxxx:{MMValue:{x:1,y:2,z:3}}
  
      let arr  = Object.entries(oldArr).map(([key, value]) => {
          const x = value.xxx == '1' ? "是" : "否";
          const y = value.yyy == '1' ? "是" : "否";
          const z = value.zzz;
          return { ...value.xxx, ID: key, xx: x,yy:y ,zz:z};
      });

