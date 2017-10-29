        
var bio = {
	"name" : "Renad Alrayes",
	"role" : "Recruiter",
	"contacts": {
		"mobile": "0552297721",
	    "email": "renad.alrayes@hotmail.com",
	    "location": "Riyadh",
},	
	"welcomeMessage": "Hi welcom",
	"skills": [
	"translation", "computer skills",],
};

var education = {
	"schools": [
	{
	    "name": "King Saud University",
		"city": "Riyadh",
		"degree": "BA",
		"majors": "English Language",
		"dates": 2014,

	},
	{
		"name": "Imam University",
		"city": "Riyadh",
		"degree": "Diploma",
		"majors": ["CS"],  
		"dates": 2015,
	}

],
"onlineCourses":[
{
	"title": "Frontend Nanodegree",
	"school": "Udacity",
	"dates": 2017,
}
]
};

var work = {
	"jobs": [
	{
		"employer": "King Saud University fo Health Scinces",
		"title": "Recruitment Officer",
		"dates": "November 2014 - August 2015",
		"description": "Recruiter",
	}
	]
};

var projects = {
	"projects": [
	{
   
		"title": "Mockup Article",
		"dates": 2017,
		"description": "transforming desgine to web page",
	}]
};

projects.projects.forEach(function (project){
   $("#projects").append(HTMLprojectStart); 
 $(".project-entry:last").append(HTMLprojectTitle.replace("%data%", projects.title), HTMLprojectDates.replace("%data%", projects.dates));

});

work.jobs.forEach(function(job){
  $("#workExperience").append(HTMLworkStart);

	var formattedEmployer = HTMLworkEmployer.replace("%data%", work.jobs [job].employer);
	var formattedTitle = HTMLworkTitle.replace("%data%", work.jobs [job].title);
	var formattedEmployerTitle = formattedEmployer + formattedTitle;

	$(".work-entry:last").append(formattedEmployerTitle);

	var formattedDates = HTMLworkDates.replace("%data%", work.jobs[job].dates);
	$(".work-entry:last").append(formattedDates);

	var formattedDescription = HTMLworkDescription.replace("%data%", work.jobs[job].description);
	$(".work-entry:last").append(formattedDescription);
});


bio.display = function() {
$("#header").prepend(HTMLheaderName.replace("%data%", bio.name));
$("#header").prepend(HTMLheaderRole.replace("%data%", bio.role));
$("#topContacts").append(HTMLmobile.replace("%data%", bio.contacts.mobile));
$("#topContacts").append(HTMLemail.replace("%data%", bio.contacts.email));
$("#topContacts").append(HTMLlocation.replace("%data%", bio.contacts.location));
};
bio.display();

school.education.forEach(function(school){
  $("#education").append(HTMLschoolStart);
  $(".education-entry:last").append(HTMLschoolName.replace("%data%", education.schools[school].name) + HTMLschoolDegree.replace("%data%", education.schools[school].degree), HTMLschoolDates.replace("%data%", education.schools[school].dates), HTMLschoolMajor.replace("%data%", education.schools[school].majors), HTMLschoolLocation.replace("%data%", education.schools[school].city));}
);


 
