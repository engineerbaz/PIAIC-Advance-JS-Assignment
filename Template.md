# Template Literals

**Template literals** are string literals allowing embedded expressions. You can use multi-line strings and string interpolation features with them


### Assignment
- Write a cover letter introducing yourself
```use personal information through variable```
  ```js
  var intro = `Post Graduated in Telecom
Lead Trainer & Technical Speaker .
adherent of academic & industry. ;
      ```
- create some varibale "coverLetter", "userName" , "date" , etc
  ```js
  var usrName= "Bashir Ahmed Zeeshan"; 
  var profession = "Engineer";
  var degree = `Master of Engineering`;
  var address = `House # 10, Block 12, Shah-re-Pakistan
  near Manzil's Stop `;
  var city = 'Karachi';
  ```
- print coverLetter value in "console.log()" ```print multi-line string literals in console.log()```
  ```js
  var cover = `Cover Letter
  ${intro}
  Name: ${usrName}
  Profession: ${profession}
  Degree: ${degree}
  City: ${city}
  Address: ${address} ` ;
  
  console.log(cover) ;
