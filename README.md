# utl-meta-analysis-of-a-single-proportion-in-R-with-forest-and-funnel-plots
Meta analysis of a single proportion in R with forest and funnel plots
    Meta analysis of a single proportion in R with forest and funnel plots                                                                          
                                                                                                                                                    
    Pooling data from 14 clinical trails and compting a pooled confidence interval on rare events.                                                  
                                                                                                                                                    
    For meta analsis R is the prefered language?                                                                                                    
                                                                                                                                                    
    Output graphics                                                                                                                                 
                                                                                                                                                    
    FULLEL PLOT                                                                                                                                     
    https://tinyurl.com/tahhjrn                                                                                                                     
    https://github.com/rogerjdeangelis/utl-meta-analysis-of-a-single-proportion-in-R-with-forest-and-funnel-plots                                   
                                                                                                                                                    
    FOREST PLOT                                                                                                                                     
    https://tinyurl.com/rgfde8h                                                                                                                     
    https://github.com/rogerjdeangelis/utl-meta-analysis-of-a-single-proportion-in-R-with-forest-and-funnel-plots/blob/master/forest.pdf            
                                                                                                                                                    
    related github                                                                                                                                  
    https://tinyurl.com/vb5jbub                                                                                                                     
    https://github.com/rogerjdeangelis/utl-meta-analysis-of-deaths-in-twenty-studies-with-forest-plot                                               
                                                                                                                                                    
    SAS COMMUNITY                                                                                                                                   
    https://tinyurl.com/v9462dd                                                                                                                     
    https://communities.sas.com/t5/Statistical-Procedures/Meta-analysis-of-proportions-using-SAS/m-p/616936                                         
                                                                                                                                                    
    macros                                                                                                                                          
    https://tinyurl.com/y9nfugth                                                                                                                    
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories                                                      
                                                                                                                                                    
                                                                                                                                                    
    I sugest you take a look at metaprop, metafor and meta                                                                                          
    I know some of these packages were developed by leading academics.                                                                              
    https://www.rdocumentation.org/packages/meta/versions/4.9-6/topics/metaprop                                                                     
                                                                                                                                                    
    *_                   _                                                                                                                          
    (_)_ __  _ __  _   _| |_                                                                                                                        
    | | '_ \| '_ \| | | | __|                                                                                                                       
    | | | | | |_) | |_| | |_                                                                                                                        
    |_|_| |_| .__/ \__,_|\__|                                                                                                                       
            |_|                                                                                                                                     
    ;                                                                                                                                               
                                                                                                                                                    
    options validvarname=upcase;                                                                                                                    
    libname sd1 "d:/sd1";                                                                                                                           
    data sd1.have;                                                                                                                                  
    input study$ country$ response sample;                                                                                                          
    cards4;                                                                                                                                         
    Batra Aus 88 199                                                                                                                                
    Berry13 US 130 250                                                                                                                              
    Berry17 US 65 170                                                                                                                               
    Black US 155 300                                                                                                                                
    Cecil Eur 125 250                                                                                                                               
    Dosa US 19 50                                                                                                                                   
    MIME Aus 185 320                                                                                                                                
    MISE US 82 130                                                                                                                                  
    KILO US 77 110                                                                                                                                  
    PERT US 50 111                                                                                                                                  
    LEPT Aus 44 180                                                                                                                                 
    ;;;;                                                                                                                                            
    run;quit;                                                                                                                                       
                                                                                                                                                    
                                                                                                                                                    
    SD1.HAVE total obs=11                                                                                                                           
                                                                                                                                                    
     STUDY      COUNTRY    RESPONSE    SAMPLE                                                                                                       
                                                                                                                                                    
     Batra        Aus          88        199                                                                                                        
     Berry13      US          130        250                                                                                                        
     Berry17      US           65        170                                                                                                        
     Black        US          155        300                                                                                                        
     Cecil        Eur         125        250                                                                                                        
     Dosa         US           19         50                                                                                                        
     MIME         Aus         185        320                                                                                                        
     MISE         US           82        130                                                                                                        
     KILO         US           77        110                                                                                                        
     PERT         US           50        111                                                                                                        
     LEPT         Aus          44        180                                                                                                        
                                                                                                                                                    
    *            _               _                                                                                                                  
      ___  _   _| |_ _ __  _   _| |_                                                                                                                
     / _ \| | | | __| '_ \| | | | __|                                                                                                               
    | (_) | |_| | |_| |_) | |_| | |_                                                                                                                
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                                               
                    |_|                                                                                                                             
    ;                                                                                                                                               
                                                                                                                                                    
    FULLEL PLOT                                                                                                                                     
    https://tinyurl.com/tahhjrn                                                                                                                     
                                                                                                                                                    
    FOREST PLOT                                                                                                                                     
    https://tinyurl.com/rgfde8h                                                                                                                     
                                                                                                                                                    
                                                                                                                                                    
    WORK.WANT total obs=30                                                                                                                          
                                                                                                                                                    
     Study     Deaths Total                Proportion       95%-CI                                                                                  
     Setting: Aus                                                                                                                                   
     Batra            88    199                 0.442 [0.372; 0.514]                                                                                
     MIME            185    320                 0.578 [0.522; 0.633]                                                                                
     LEPT             44    180                 0.244 [0.184; 0.314]                                                                                
     Subtotal               699                 0.454 [0.417; 0.491]                                                                                
     Heterogeneity: I 2 = 94%, p < 0.01                                                                                                             
                                                                                                                                                    
     Setting: US                                                                                                                                    
     Berry13         130 250                    0.520 [0.456; 0.583]                                                                                
     Berry17          65 170                    0.382 [0.309; 0.460]                                                                                
     Black           155 300                    0.517 [0.459; 0.574]                                                                                
     Dosa             19  50                    0.380 [0.247; 0.528]                                                                                
     MISE             82 130                    0.631 [0.542; 0.714]                                                                                
     KILO             77 110                    0.700 [0.605; 0.784]                                                                                
     PERT             50 111                    0.450 [0.356; 0.548]                                                                                
     Subtotal              1121                 0.516 [0.486; 0.545]                                                                                
     Heterogeneity: I 2 = 86%, p < 0.01                                                                                                             
                                                                                                                                                    
     Setting: Eur                                                                                                                                   
     Cecil          125     250                 0.500 [0.436; 0.564]                                                                                
     Subtotal               250                 0.500 [0.438; 0.562]                                                                                
     Heterogeneity: not applicable                                                                                                                  
                                                                                                                                                    
     Total                 2070                 0.493 [0.471; 0.514]                                                                                
     Heterogeneity: I = 91%, p < 0.01                                                                                                               
     Residual heterogeneity: I 2 0.2    p < 0.4                                                                                                     
                                                                                                                                                    
    *          _       _   _                                                                                                                        
     ___  ___ | |_   _| |_(_) ___  _ __                                                                                                             
    / __|/ _ \| | | | | __| |/ _ \| '_ \                                                                                                            
    \__ \ (_) | | |_| | |_| | (_) | | | |                                                                                                           
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|                                                                                                           
                                                                                                                                                    
    ;                                                                                                                                               
                                                                                                                                                    
    %utl_submit_r64('                                                                                                                               
    library(meta);                                                                                                                                  
    library(haven);                                                                                                                                 
    library(metafor);                                                                                                                               
    library(SASxport);                                                                                                                              
    library(funnelR);                                                                                                                               
    have<-read_sas("d:/sd1/have.sas7bdat");                                                                                                         
    have;                                                                                                                                           
    studies <- have$STUDY;                                                                                                                          
    obs     <- have$RESPONSE;                                                                                                                       
    denom   <- have$SAMPLE;                                                                                                                         
    setting <- have$COUNTRY;                                                                                                                        
    m1 <- metaprop(obs, denom, studies, comb.random=F, byvar=setting,                                                                               
                   bylab="Setting", byseparator=": ");                                                                                              
    m2 <- metaprop(obs, denom, studies, comb.random=F, byvar=setting,                                                                               
                   bylab="Setting", byseparator=": ", method="GLMM");                                                                               
    m2$w.fixed <- m1$w.fixed;                                                                                                                       
    pdf("d:/pdf/forest.pdf",width = 10, height =8);                                                                                                 
    forest(m2, print.tau2 = FALSE, col.by="black", text.fixed = "Total",                                                                            
           text.fixed.w = "Subtotal", rightcols = c("effect","ci"), digits=3L,                                                                      
           leftlabs=c("Study","Deaths","Total"));                                                                                                   
    pdf();                                                                                                                                          
    colnames(have)<-c("id","country","n","d");                                                                                                      
    flimits   <- fundata(input=have,                                                                                                                
              benchmark=0.50,                                                                                                                       
              alpha=0.80,                                                                                                                           
              alpha2=0.95,                                                                                                                          
              method="approximate",                                                                                                                 
              step=1);                                                                                                                              
    funnelPlt  <- funplot(input=have,flimits);                                                                                                      
    pdf("d:/pdf/funnel.pdf",width = 10, height =8);                                                                                                 
    funnelPlt;                                                                                                                                      
    pdf();                                                                                                                                          
    ');                                                                                                                                             
                                                                                                                                                    
                                                                                                                                                    
    * scape the pdf to create want SAS dataset;                                                                                                     
    %utl_submit_r64('                                                                                                                               
    library("tm");                                                                                                                                  
    library(SASxport);                                                                                                                              
    file <- "d:/pdf/forest.pdf";                                                                                                                    
    Rpdf <- readPDF(control = list(text = "-layout"));                                                                                              
    corpus <- VCorpus(URISource(file),                                                                                                              
          readerControl = list(reader = Rpdf));                                                                                                     
    want <- as.data.frame(content(content(corpus)[[1]]));                                                                                           
    colnames(want)<-"lines";                                                                                                                        
    lines <- as.data.frame(strsplit(as.character(want$lines), split="\\r\\n"));                                                                     
    colnames(lines)<-"lines";                                                                                                                       
    str(lines);                                                                                                                                     
    lines[] <- lapply(lines, function(x) if(is.factor(x)) as.character(x) else x);                                                                  
    write.xport(lines,file="d:/xpt/lines.xpt");                                                                                                     
    ');                                                                                                                                             
                                                                                                                                                    
    * convert from VR transport to SAS dataset;                                                                                                     
    libname xpt xport "d:/xpt/lines.xpt";                                                                                                           
    data want;                                                                                                                                      
      set xpt.lines;                                                                                                                                
    run;quit;                                                                                                                                       
    libname xpt clear;                                                                                                                              
                                                                                                                                                    
                                                                                                                                                    
