# Quiz
Java-based quiz with use of Array, for Loop, Scanner input, nested If (else if) statement. Changes the final score and final outcome on basis of answers typed in by user.


package Quiz;

import java.util.Scanner;
import java.util.Arrays;




public class questions2 {

	public static void main(String[] args) {
		Scanner scanner = new Scanner (System.in);
		
		System.out.println("Please type in a, b, or c to choose one of following answers that describes best your feelings:"
				+ "\na) I definitely agree\nb) I Neither agree or disagree\nc) I definitely disagree\n\nQUESTION:");
				
		
		String [] questions = {
				"I am fine depending on my partner.",
				"I crave sense of closeness, both physical and emotional.",
				"It's very easy for me to open up to my partner",
				"I am afraid to be abbandoned by my partner.",
				"I wam afraid I care more about the other person than she/he does care about me.",
				"I feel like I love my partners more than they do love me.",
				"I think the urge to be close with my partner scared away some people from me"
				};
		
		Integer score = 0;
		
	for (int i=0; i<questions.length; i++) {
		//int size = questions.length;
		
	
		System.out.println(questions[i]);
		String answer = scanner.nextLine();
		
		String a ="a";
		String b ="b";
		String c ="c";
		
		
		
		
		if(answer.equals(a)) {
			score++;
		}
		if(answer.equals(c)) {
			score--;
		}
		
	}
		
		
		System.out.println("Your score is " + score + " out of " + questions.length);
		
		
	if (score>=-7 && score<=-2) {
			System.out.println("You are avoidant type");
			}
			else if(score>=-1 && score<=3) {
			System.out.println("You are secure type");
			}
			else {
			System.out.println("You are anxious type");
			}

	
		System.out.println("To get to know more speak to your therapist or take a real test:http://www.web-research-design.net/cgi-bin/crq/crq.pl"); 
	
		scanner.close();
	
		}
}
