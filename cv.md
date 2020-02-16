# RESUME 
## Wioletta Nosenko 
* phone, telegram: +375296019352 (A1) 
* mail: violetta.nosenko@gmail.com 
### Summary 
My purpose is to learn how to create quality web pages, my product must be pretty and logical constructed. I want to become demanded worker in this direction, because i love creative tasks. My features, that can help me to reach goal: responsability, creativity, thirst for knowledge, moderate perfectionism. 
### Skills 
Have experience in C, C++, Java, Assembler languages, in UML diagrams and sowtware requirements writing. Have skills in algothmics tasks. 
### Code examples 
This is my class PayconditionSelector, that is a graphical form for selecting pay condition in tender: 

```java 
public class PayConditionSelector { 

private static final int STANDART_WIDTH = 270; 

private static final int STANDART_HEIGHT = 100; 

private static final int NUMBER_INPUT_WIDTH = 40; 

private static final int STANDART_SPACE = 5; 



private String memberName; 

private PayCondition payCondition; 



public PayConditionSelector(String memberName, PayCondition payCondition){ 

this.memberName = memberName; 

this.payCondition = payCondition; 

Stage stage = new Stage(); 

start(stage); 

} 



public void start(Stage stage) { stage.setTitle(memberName); 

stage.setResizable(false); 



IntegerComboBox prePayPrecent = new IntegerComboBox(0,100); 

prePayPrecent.setValue(0); 

prePayPrecent.setMinWidth(NUMBER_INPUT_WIDTH + 20); 

TextField prePayDays = new TextField(); 

prePayDays.setOnKeyPressed(keyEvent -> { 

if (keyEvent.getCode() == KeyCode.ENTER){ 

try { 

reformDaysField(prePayDays); 

} catch(NumberFormatException e){ 

prePayDays.clear(); 

} 

} 

}); 

prePayDays.setPrefWidth(NUMBER_INPUT_WIDTH); 

HBox prePayLine = new HBox(); 

prePayLine.setSpacing(STANDART_SPACE); 

prePayLine.getChildren().addAll(new Label("Аванс: "),prePayPrecent, 

new Label ("% в течение(дни) "),prePayDays); 



TextField factPayDays = new TextField(); 

factPayDays.setPrefWidth(NUMBER_INPUT_WIDTH); 

factPayDays.setOnKeyPressed(keyEvent -> { 

if (keyEvent.getCode() == KeyCode.ENTER){ 

try { 

reformDaysField(factPayDays); 

}catch(NumberFormatException e){ 

factPayDays.clear(); 

} 

} 

}); 

HBox factPayLine = new HBox(); 

factPayLine.setSpacing(STANDART_SPACE); 

factPayLine.getChildren().setAll(new Label("По факту в течение(дни) "), factPayDays); 



Button saveButton = new Button("Сохранить"); 

saveButton.setMinWidth(30); 

saveButton.setOnMouseClicked(new EventHandler<MouseEvent>() { 

@Override 

public void handle(MouseEvent mouseEvent) { 

int preDays; 

int factDays; 

try { 

preDays = Integer.parseInt(prePayDays.getText()); 

}catch(NumberFormatException e){ 

preDays = 0; 

} 

try { 

factDays = Integer.parseInt(factPayDays.getText()); 

}catch(NumberFormatException e){ 

factDays = 0; 

} 

payCondition.setPayCondition(prePayPrecent.getValue(), 

preDays, factDays); 

stage.close(); 

} 

}); 

HBox buttonLine= new HBox(); 

buttonLine.setAlignment(Pos.CENTER); 

buttonLine.getChildren().add(saveButton); 



VBox mainLayout = new VBox(); 

mainLayout.setPadding(new Insets(STANDART_SPACE)); 

mainLayout.setSpacing(STANDART_SPACE); 

mainLayout.getChildren().setAll(prePayLine,factPayLine,buttonLine); 



Scene scene = new Scene(mainLayout,STANDART_WIDTH,STANDART_HEIGHT); 

stage.setScene(scene); 

stage.show(); 

} 



void reformDaysField (TextField textField) throws NumberFormatException { 

int iDays = Integer.parseInt(textField.getText()); 

if (iDays<0) { iDays -= iDays; } 

String sDays =""; 

sDays+=iDays; 

textField.setText(sDays); 

} 

} 
``` 
### Experience 
* Addresbook in C++ and Qt with graphical interface 
* Programm [Tendro](https://github.com/WioWio/Tendro) for calculating winners of tenders for belorussian state enterprises with gr.int. (Java 11, Eclipse, using MVC pattern). 
* Unit tests for complex numbers calculator 
### Education 
2.5 years of bachelor at the Belorussian State University of informatics and radionics. 
### Languages 
* English: reading and writing intermediate level, speaking and listening pre-intermediate 
* German: upper-intermediate
