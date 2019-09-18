# Norm 1 Normalization Process for Veterinary Office
## Each table contains a single theme. Each record is unique.
R1= PetName(PetType, PetBreed, PetDOB, OwnersLastName, OwnersFirstName, OwnerPhone, OwnerEmail, Service, Date, Charge)

# Norm 2 PrimaryKey Found

R12a = **PetName** (PetType, PetBreed, PetDOB, **OwnersLastName**, OwnersFirstName, OwnerPhone, OwnerEmail, **Service**, Date, Charge)

R12b= PetName(PetType, PetBreed, PetDob, PetID)
OwnersLastName(OwnersFirstName, OwnerPhone, OwnerEmail, OwnerID)
Service (Date,Charge,ServiceID)

# Norm 3 ID Relations

R13b = PetName (PetID, PetType, PetBreed, PetDOB)
OwnersLastName(OwnerID, OwnersFirstName, OwnerPhone, OwnerEmail, PetID)
Service (ServiceID, Date, Charge, PetID, OwnerID)
