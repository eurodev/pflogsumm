# Postfix Log Entry Summarizer

pflogsumm.pl is designed to provide an over-view of postfix activity, with just enough detail to give the administrator a "heads up" for potential trouble spots. The following is an over-view of the reports produced:

* Total number of:
  * Messages received, delivered, forwarded, deferred, bounced and rejected
  * Bytes in messages received and delivered
  * Sending and Recipient Hosts/Domains
  * Senders and Recipients
  * Optional SMTPD totals for number of connections, number of hosts/domains connecting, average connect time and total connect time
* Per-Day Traffic Summary (for multi-day logs)
* Per-Hour Traffic (daily average for multi-day logs)
* Optional Per-Hour and Per-Day SMTPD connection summaries
* Sorted in descending order:
  * Recipient Hosts/Domains by message count, including:
    * Number of messages sent to recipient host/domain
    * Number of bytes in messages
    * Number of defers
    * Average delivery delay
    * Maximum delivery delay
  * Sending Hosts/Domains by message and byte count
  * Optional Hosts/Domains SMTPD connection summary
  * Senders by message count
  * Recipients by message count
  * Senders by message size
  * Recipients by message size with an option to limit these reports to the top nn.
* A Semi-Detailed Summary of:
  * Messages deferred
  * Messages bounced
  * Messages rejected
* Summaries of warnings, fatal errors, and panics
* Summary of master daemon messages
* Optional detail of messages received, sorted by domain, then sender-in-domain, with a list of recipients-per-message.
* Optional output of "mailq" run

Pflogsumm.pl was written using Perl 5.004. As of version 19990413-02, pflogsumm worked with Perl 5.003, but future compatibility is not guaranteed.

Pflogsumm.pl requires the Date::Calc module, which can be obtained here.

Production versions have been tested more thoroughly, at more sites. Beta versions are the result of enhancement requests and bug reports. While also believed to produce correct results (maybe even more accurate or better results--depending on the reason for the change), they're labeled beta until I get enough feedback to let me know all's well. (Or I fail to get any negative feed-back in the form of bug-reports.)>
