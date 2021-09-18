[9/18, 2:50 PM] Ankit Mishra: stackType s1 = createStack(3);
	stackType s2 = createStack(5);
	push( 10, &s1);
	push( 20, &s1);push( 30, &s1);
	push( 25, &s2);push( 35, &s2);push( 45, &s2);
	peeked_ele = peek(s1);
	printf("\n Peeked element from s1: %d", peeked_ele );
	peeked_ele = peek(s2);
	printf("\n Peeked element from s2: %d", peeked_ele );
[9/18, 2:50 PM] Ankit Mishra: //Pop
	popped_ele = pop(&s1);
	printf("\n Popped element from s1: %d", popped_ele );
	popped_ele = pop(&s2);
	printf("\n Popped elementfrom s2: %d", popped_ele );
	//PEEK
	peeked_ele = peek(s1);
	printf("\n Peeked element from s1: %d", peeked_ele );
	peeked_ele = peek(s2);
	printf("\n Peeked element from s2: %d", peeked_ele );
