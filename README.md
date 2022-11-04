1.2. შექმენით ინტერფეისი Student შემდეგი ველებით
   •	Id: string (guid, generated using https://www.npmjs.com/package/uuid)
   •	firstName: string
   •	lastNAme: string
   •	personalNumber: string
   •	address: {cityId: number, street: string}
1.2. შექმენით ინტერფეისი City შემდეგი ველებით
   •	id: number
   •	name: string
1.3. შექმენით ინტერფეისი StudentFilter შემდეგი ველებით
   •	firstName
   •	lastName
   •	personalNumber
1.4. შექმენით SearchOptions ინტერფეისი შემდეგი ველებით
   •	enableTotalRecordsLimit: boolean
   •	maxSearchResoultItemCount: number
2. შექმენით სერვისი CityService შემდეგი მეთოდით
   •	getCities(): City[] რომელიც დააბრუბს ქალაქების სიას
გადაწყვიტეთ სად უნდა დარეგისტრიროთ სერვისი (რუთში თუ კომპონენტში)
3. შექმენით სერვისი StudentService, სტუდენტების სიის private property-ით , რომელსაც ექნება შემდეგი მეთოდები
   •	addStudent(s: Student): String - სიაში სტუდენტის ჩამატება
   •	removeStudent(id: string) - სიიდან სტუდენტის წაშლა
   •	updateStudent(s: Student) - სიაში სტუდენტის განახლება, თუ არსებობს
   •	getStudents():Student[] - სტუდენტების სიის დაბრუნება
  გადაწყვიტეთ სად უნდა დარეგისტრიროთ სერვისი (რუთში თუ კომპონენტში)
4. შექმენით StudentSearchService 
   •	filterStudents(filter: StudentFilter). გამოიყენეთ სტუდენტების სია StudentsSerivice-დან. ფილტრი უნდა მუშაობდეს შემდეგნაირად: firstName და lastName-ს შეიძლება შეიცავდეს ნაწილობრივ, personalNumber უნდა ემთხვეოდეს ზუსტად. 
   o	SearchOptions-ის დეფოულტ კონფიგი უნდა გამოიყენოს (injected in constructor).
   o	თუ enableTotalRecordsLimit არის true, მაშინ შედეგები შეზღუდულია, უნდა დააბრუნოს maxSearchResultItemCount რაოდენობის ტოპ ჩანაწერები
5. შექმენით სტუდენტის  კომპონენტი.  შექმენით სტუდენტის დამატების ფორმა შემდეგი ველებით. firstName, lastName, personal number და address. ყველა ველი სავალდებულოა.
როდესაც დაადასტურებთ, student service-დან უნდა გამოიძახოთ  addStudent მეთოდი. თუ სტუდენტი უკვე არსებობს (personal number –ის მიხედვით) გამოისროლეთ ერორი.
6. შექმენით student list კომპონენტი, რომელიც გამოიტანს სტუდენტების სიის ცხრილს. დაამატეთ წაშლის ღილაკი თითოეულ სტრიქონზე. კომპონენტში სტუდენტების სია student service-ის getStudents მეთოდის საშუალებით წამოიღეთ.
7. გააკეთეთ წაშლის ფუნქციონალი student service-ის deleteStudent მეთოდის გამოყენებით.
8. დაამატეთ Advanced Student search component შემდეგი ველებით: firstName, lastName, personalNumber და ღილაკი: search და რესეტ.
   •	გამოიყენეთ studentSearchService ძებნის ფუნქციონალის იმპლემენტაციისთვის.

