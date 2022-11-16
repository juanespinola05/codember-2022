```javascript
function isValid(user, fields) {
  const joined = user.join('')
  return fields.every(field => joined.includes(field))
}

const fields = ['usr','eme','psw','age','loc','fll']

const noBreaks = db.split(/\n/)
let users = []
let user = []
for(item of noBreaks) {
  if(!item) {
    users.push(user)
    user = []
    continue
  }
  user.push(item)
}
const valid = users.filter(user => isValid(user, fields))
let lastUser = valid.at(-1)
let count = valid.length
```