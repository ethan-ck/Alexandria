	scriptName esqToggleCaravan as Quest
	
	; defining variables 
	ReferenceAlias Property Alias_esqCaravanBanditLeader Auto  
	ReferenceAlias Property Alias_esqBrokenWagon  Auto  
	ReferenceAlias Property Alias_esqBarrel01  Auto  
	ReferenceAlias Property Alias_esqBarrel02  Auto  
	ReferenceAlias Property Alias_esqCaravanBandit01  Auto  
	ReferenceAlias Property Alias_esqCaravanBandit02  Auto  
	ReferenceAlias Property Alias_esqCaravanAmbush  Auto  
	ReferenceAlias Property Alias_esqFrank  Auto  
	Quest property esqQuest auto 
	
	Function esqEnableCaravan()

	; creates an array of aliases
	ReferenceAlias[] esqCaravanArray 
		
		; assign each index an element 
		esqCaravanArray[0] = Alias_esqCaravanBanditLeader ; caravan bandit leader
		esqCaravanArray[1] = Alias_esqBrokenWagon	; broken wagon 
		esqCaravanArray[2] = Alias_esqBarrel01 	 ; first barrel 
		esqCaravanArray[3] = Alias_esqBarrel02		; second barrel 
		esqCaravanArray[4] = Alias_esqCaravanBandit01    ; first caravan bandit 
		esqCaravanArray[5] = Alias_esqCaravanBandit02	; second caravan bandit 
		esqCaravanArray[6] = Alias_esqCaravanAmbush   ; caravan marker 
		esqCaravanArray[7] = Alias_esqFrank; frank 

		; Will check which stage the quest is at and either enable/disable the caravan objects 

		If esqQuest.GetStage() == 20
			Int esqElement = esqCaravanArray.Length
			int esqIndex = 0
			While esqIndex < esqElement
				esqCaravanArray[esqIndex].GetReference().Enable()
				esqIndex += 1
			endWhile

		elseIf esqQuest.GetStage() == 30
			Int esqElement = esqCaravanArray.Length
			int esqIndex = 0
			While esqIndex < esqElement
				esqCaravanArray[esqIndex].GetReference().Disable()
				esqIndex += 1
			endWhile
		endIf

	endFunction