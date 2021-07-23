# Vote4Change
A online voting platform for performing elections

constraint applied
Alter table user_details add constraint ud_an_pk primary key(adhar_no);

Alter table candidate add constraint cd_cid_pk primary key(candidate_id);

Alter table candidate add constraint cd_uid_fk foreign key(user_id) references user_details(adhar_no);

Alter table voting add constraint vt_cid_fk foreign key(candidate_id) references candidate(candidate_id);

Alter table voting add constraint vt_vid_pk primary key(voter_id);

Alter table voting add constraint vt_vid_fk foreign key(voter_id) references user_details(adhar_no);





