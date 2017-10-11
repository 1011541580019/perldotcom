{
   "title" : "Perl Unicode Cookbook: Enable UTF-8 Literals",
   "description" : "â 3: Declare source in UTF-8 for identiï¬ers and literals Without the all-critical use utf8 declaration, putting UTFâ8 in your literals and identiï¬ers won't work right. If you used the standard Perl Unicode preamble, this already happened. If you did,...",
   "thumbnail" : null,
   "categories" : "unicode",
   "authors" : [
      "tom-christiansen"
   ],
   "image" : null,
   "draft" : null,
   "tags" : [],
   "date" : "2012-04-06T06:00:01-08:00",
   "slug" : "/pub/2012/04/perlunicook-enable-utf-8-literals"
}





â 3: Declare source in UTF-8 for identiï¬ers and literals {#Declare-source-in-utf8-for-identifiers-and-literals}
--------------------------------------------------------

Without the all-critical `use utf8` declaration, putting UTFâ8 in your
literals and identiï¬ers won't work right. If you used [the standard Perl
Unicode
preamble](/media/_pub_2012_04_perlunicook-enable-utf-8-literals/perlunicook-standard-preamble.html),
this already happened. If you did, you can do things like this:

    use utf8;

     my $measure   = "ÃngstrÃ¶m";
     my @Î¼soft     = qw( cp852 cp1251 cp1252 );
     my @á½ÏÎ­ÏÎ¼ÎµÎ³Î±Ï = qw( á½ÏÎ­Ï  Î¼ÎµÎ³Î±Ï );
     my @é¯        = qw( koi8-f koi8-u koi8-r );
     my $motto     = "ðª ð ðª"; # FAMILY, GROWING HEART, DROMEDARY CAMEL

If you forget `use utf8`, high bytes will be misunderstood as separate
characters, and nothing will work right. Remember that this pragma only
affects the interpretation of *literal* UTF-8 in your source code.

Previous: [â 2: Fine-Tuning Unicode
Warnings](/media/_pub_2012_04_perlunicook-enable-utf-8-literals/perl-unicook-fine-tuning-warnings.html)

Series Index: [The Standard
Preamble](/media/_pub_2012_04_perlunicook-enable-utf-8-literals/perlunicook-standard-preamble.html)

Next: [â 4: Characters and Their
Numbers](/media/_pub_2012_04_perlunicook-enable-utf-8-literals/perlunicook-chars-and-their-nums.html)


