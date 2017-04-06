# Tyler Moon
A simple landing page / resume website

Address: 215 Spencer Pl Apt. 512A, Cayce, SC 29033

Phone Number: 803-792-2216

Email: moon.tyler@gmail.com 

GitHub: [https://github.com/tmoon8730]()

Resume: [TylerMoonResume2017](https://github.com/tylermoon/tylermoon.github.io/blob/master/TylerMoonResume2017.pdf)

## Technical Skills

| Standard Languages                                               | Web Development                                          |  IDE's and Tools                           | Scripting Languages | Mobile Development |
|:-----------------------------------------------------------------|:---------------------------------------------------------|:-------------------------------------------|:--------------------|:-------------------|
| [Java](https://en.wikipedia.org/wiki/Java_(programming_language))| [HTML](http://www.w3schools.com/html/html_intro.asp)     | [Eclipse](https://eclipse.org/)             | [Python](https://www.python.org/) | [Android Development](https://www.android.com/)|
| [C](https://en.wikipedia.org/wiki/C_(programming_language))| [CSS](http://www.w3schools.com/css/css_intro.asp) | [XCode](https://developer.apple.com/xcode/) | [Perl](https://www.perl.org/) | [iOS Development](https://developer.apple.com/programs/)|             
| [C++](http://www.cplusplus.com/) | [LAMP Stack](https://en.wikipedia.org/wiki/LAMP_(software_bundle)) (Linux, Apache, MySQL and PHP/Python/Perl)    | [Visual Studio](https://www.visualstudio.com/)| [Bash](https://www.gnu.org/software/bash/) | [MacOS Development]((https://developer.apple.com/programs/))  |
| [C#](https://msdn.microsoft.com/en-us/library/kx37x362.aspx) | [MEAN Stack](http://mean.io/) (MongoDB, ExpressJS, AngularJS, and Node.js)  | [Spring Tool Suite](http://spring.io/tools/sts)| [Ruby](https://www.ruby-lang.org/en/) |                    |
| [Objective C](https://www.tutorialspoint.com/objective_c/)| [MeteorJS](https://www.meteor.com/) | [Atom](https://atom.io/) | [Markdown](https://en.wikipedia.org/wiki/Markdown) |                    |
| [Swift](https://developer.apple.com/swift/) | [ASP.NET MVC](https://msdn.microsoft.com/en-us/library/dd381412(v=vs.108).aspx) | [Amazon AWS](https://aws.amazon.com/)  |                     |                    |
| [Spring Boot](http://spring.io/) | [Firebase](https://firebase.google.com/)                                                         | [Digital Ocean Servers](https://www.digitalocean.com/)    |                     |                    |

* * *

# Work Experience

### [Avidxchange: Software Development Intern (2016)](https://www.avidxchange.com/)
- Researched, designed, and built a prototype IVR automation solution using a C# ASP.Net MVC application, Twilio Cloud API, and Authy Cloud API
- Developed a two factor authentication system
- Designed and built a web automation framework using C# and Selenium
- Built a Node.js and MongoDB website for testing bill payment automation systems

### [Center for Digital Humanities: System Administration & Software Development (2016)](https://sc.edu/about/centers/digital_humanities/)
- Responsible for maintaining and backing up development and production servers
- Implemented source control, virtual private servers, and Docker containers
- Worked on Meteor.js application for touchscreen displays in USC Museum

### [Perahealth: Software Development Intern (2015)](http://www.perahealth.com/)
- In an Agile Development process, drastically overhauled an AngularJS web application with the Highcharts charting library and a SQL database
- Fixed Javascript and AngularJS bugs in several projects
- Created a Java program to simulate data feeds for testing software
- Created an iOS application with a Java data api to access a SQL database

### [3D Systems: Quality Assurance Intern (2013 – 2014)](http://www.3dsystems.com/)
- Responsible for testing software and firmware for 3D Printers
- Helped create and implement testing plans for printer software and firmware
- Created an automated GUI testing system using Sikuli
- Assisted developers in fixing minor bugs using C# and XAML

* * *

# Education

### College
- University of South Carolina
- Expected graduation date: Spring 2018
- Major: Computer Science

### High school
- Homeschooled
- Graduated Spring 2014
- Dual Enrollment College - High school 2012 - 2014
  - York Technical College
  - Grand Caynon University (Online)
  - San Jose State University (Online)

* * *

# Side Projects
Since I was around 11 or 12 years old I have been interested in programming and software development. The best way to learn a new programming language or technique is to do a few tutorials or build a side project with that language or technology. Over the years many I have built many side projects and most of them consisted of following tutorials. Listed below are the details for a few of the bigger and more interesting projects that I have completed.

## MEIRLBOT
- Source Code: [GitHub](https://github.com/tmoon8730/meirlbot.git)
- Description: The MEIRLBOT is a set of Java Spring Boot applications for the purpose of creating and displaying memes. The main reason for creating this project was to learn new technologies and build resumes.
- Technical Spec: Java Spring Boot Application
- Code Example:

Java Spring Boot
``` java
@SpringBootApplication
public class MemeExchangeApplication {

  public static void main(String[] args) {
    SpringApplication.run(MemeExchangeApplication.class, args);
  }
}
```

## Nutriments
- Website: [http://nutrimentsapp.com/](http://nutrimentsapp.com/)
- Source Code: [GitHub](https://github.com/tmoon8730/FATStats)
- Description: Nutriments is an iOS Application for simple and quick exercise and supplement tracking
- Technical Spec: iOS Application developed in Swift
- Code Example:

Swift
``` swift
func createDrive(managedContext: NSManagedObjectContext, quarter: String, time: String, yardLine: String) -> Bool{
    let entityDrive = NSEntityDescription.entityForName("DriveEntity", inManagedObjectContext: managedContext)
    let newDrive = DriveEntity(entity: entityDrive!, insertIntoManagedObjectContext: managedContext)
    newDrive.quarter = quarter
    newDrive.time = time
    newDrive.yardLine = yardLine
    do{
        try newDrive.managedObjectContext?.save()
        print("New drive added: \(newDrive.quarter!) with \(newDrive.time!) left on the \(newDrive.yardLine!) yard line")
        return true
    }catch{
        let saveError = error as NSError
        print(saveError)
    }
    return false
}
```


## AndroidMultiTool
- Source Code: [GitHub](https://github.com/tmoon8730/androidmultitool)
- Description: A Android Application with a slew of different useful tools including:
  - Alarm Clock
  - Custom Web Browser
  - Email App
  - Present Fortune Teller
  - A Database Access Object
- Technical Spec: Java Application developed in Java
- Code Example:

Java
``` java
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_alarm_manager);
        Toolbar toolbar = (Toolbar) findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);

        alarm = new AlarmManagerBroadcastReceiver();

        FloatingActionButton fab = (FloatingActionButton) findViewById(R.id.fab);
        fab.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Snackbar.make(view, "Replace with your own action", Snackbar.LENGTH_LONG)
                        .setAction("Action", null).show();
            }
        });
    }
```

## VCF Gene Parser
- Source Code: [GitHub](https://github.com/tmoon8730/VCFGeneParser)
- Description: This is a simple project for parsing VCF files with gene information with a Python script and searching it through a NodeJS website. The VCF file is commonly used for transferring gene data and this tool easily stores the data in a MongoDB database for easier analysis than the flat file VCF.
- Technical Spec: Python Script and NodeJS Express Website
- Code Example:

Python
``` python
def saveToMongo(record):
    post = {
    "chrom": record.CHROM,
    "pos": record.POS,
    "gene_id": record.ID,
    "ref": record.REF,
    "alt": record.ALT,
    "qual": record.QUAL,
    "info": record.INFO,
    "samples": record.samples
    }
    insertedId = collection.insert_one(post).inserted_id
    print('Inserted post with id: %s' % insertedId)
```

NodeJS
``` javascript
// Get the gene_id when the text field is submitted
app.post('/', function(req, res){
	console.log(req.body.gene_id);
	// Query the mongo database
	Gene.findOne({gene_id: req.body.gene_id}, function(err, gene){
		if(gene != null){
			if(err){
				res.render('index', {title:'Hey', message: "Error finding a Gene for " + req.body.gene_id, geneId: 'n/a', chrom: 'n/a', pos: 'n/a'});
				console.log(err);
			}
			console.log("found id %s", gene.gene_id);
			// Render the index page and pass in all the data for the gene
			res.render('index', {title:'Hey', message: "Found a Gene for " + gene.gene_id,
			geneId: gene.gene_id, chrom: gene.chrom, pos: gene.pos, ref: gene.ref, alt: gene.alt});
		}else{
			res.render('index', {title:'Hey', message: 'Could not find a gene for ' + req.body.gene_id,
			geneId: 'n/a', chrom: 'n/a', pos: 'n/a', ref: 'n/a', alt: ['n/a','n/a']});
		}
	})
});
```

## SCS Android App
- Source Code: [GitHub](https://github.com/tmoon8730/SCS)
- Description: 
- Technical Spec: Android Application with real time [Firebase](https://firebase.google.com/) database
- Code Example:

Java (Android):
``` java
    /*
    * This method returns a integer value for the given index in the Firebase database.
    * Uses a callback listener to handle returning data from an async thread
    */
    public void getIndexValue(String reference, final String indexName, @NonNull final SimpleCallback<Integer> finishedCallback){
        DatabaseReference courseRef = firebaseDatabase.getReference(reference).child(indexName);
        courseRef.addValueEventListener(new ValueEventListener() {
            @Override
            public void onDataChange(DataSnapshot dataSnapshot) {
                // This will simple call the callback interface SimpleCallback.java
                try {
                    finishedCallback.callback(dataSnapshot.getValue(Integer.class));
                    System.out.println("Returning " + dataSnapshot.getValue(Integer.class) + " " + indexName);
                }catch(Exception e){
                    e.printStackTrace();
                }
            }

            @Override
            public void onCancelled(DatabaseError databaseError) {
                // TODO: Add onCancelled stuff
            }
        });
    }

```
