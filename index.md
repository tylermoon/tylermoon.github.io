---
layout: default
---
# [Resume]()

## [](#header-1)**Technical Summary**

* _Language_: Java, C++, C#, Swift, HTML, CSS, JavaScript, Java, XML, Python
* _Platform_: Android (Java, XML), iOS(XCode, Swift), SAAS (Java Spring, ASP.NET MVC)
* _GIS_: ArcGIS, ArcMap, MySQL (with geo-plugin)
* _Operating System_: Mac, Windows, Linux
* _Cloud Systems_: Google Cloud, Amazon AWS, Azure Cloud, Digital Ocean

## [](#header-1)**Professional Experience**

**Avidxchange - Charlotte , NC				-				July 2016 - August 2017**

_Software Development Intern								July 2017 - August 2017_

- Refactored MVC controllers to Web API controllers in an enterprise code refactoring effort
- Researched, designed, and implemented a NuGet library to standardize cross service communication for multiple teams using RabbitMQ
- Collaborated with a fellow intern in a paired-programming prototype project

_Software Development Intern								July 2016 - August 2016_

- Researched, designed, and built a prototype IVR automation program with a two factor authentication system
- Designed and built a web automation framework using C# and Selenium as well as a Node.js and MongoDB website for testing the framework

**Center for Digital Humanities - Columbia, SC						January 2016 - Present**

_System Administration Intern								August 2016 - May 2017_

- Responsible for setting up,  maintaining and backing up development and production servers
- Implemented source control, virtual private servers, and Docker containers.
- Worked on a Meteor.js web-application for touchscreen displays in the USC Museum

_Web Development Intern									January 2016 - May 2016_

- Worked on several PHP and JavaScript website projects
- Completed initial research into Docker containerization

**Perahealth - Charlotte, NC								May 2015 - December 2015**

_Software Development Intern_

* In an Agile Development process, drastically overhauled an AngularJS web application with the Highcharts charting library and a SQL database
* Fixed Javascript and AngularJS bugs in several projects
* Created a Java program to simulate data feeds for testing software
* Created an iOS application with a Java data api to access a SQL database

**3D Systems - Rock Hill, SC								October 2013 - August 2014**

_Quality Assurance Intern_

* Responsible for testing software and firmware for 3D Printers
* Helped create and implement testing plans for printer software and firmware
* Created an automated GUI testing system using Sikuli
* Assisted developers in fixing minor bugs using C# and XAML



## [](#header-1)**Education**

- University of South Carolina – Columbia, SC						May 2018
- Bachelors of Computer Science with a Concentration in Geographic Information Systems
- Current GPA: 3.1
- USC Dean’s List - Fall 2014
- President of CSCC Club - Fall 2015 to Present

---

# [Side Projects]()
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
