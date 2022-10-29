# Moongoose-Validations
------------------------------------------
Validations Resource: https://mongoosejs.com/docs/validation.html
------------------------------------------

// Example validation for User 


  `const UserSchema = new mongoose.Schema(
  
    {
    
        first_name:{
        
            type: String,
            
            required: [true, 'First name is required'],
            
            minlength: [6, 'First name must be at least 6 characters long']
            
        },
        
        last_name:{
        
            type: String,
            
            required: [true, 'Last name is required'],
            
            minlength: [6, 'Last name must be at least 6 characters long']
            
        },
        
        age:{
        
            type: Number,
            
            min: [18, "You must be 18 or older to register"],
            
            max: [150, "You must be at most 149 years old to register"]
            
        },
        
        email: { type: String, required: [true, "email is required"]}
        
    },
    
    {timestamps: true}
    
  );`
