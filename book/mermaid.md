```{mermaid}

    flowchart TD
        
        covid_victims([Covid Victims]) --- covid_victims_covid_victim[Covid Victim]
        click covid_victims_covid_victim href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/covid_victims/covid_victim-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_affiliation[Affiliation]
        click hungarian_elections_affiliation href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/affiliation-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_candidate[Candidate]
        click hungarian_elections_candidate href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/candidate-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_nominating_organization[Nominating Organization]
        click hungarian_elections_nominating_organization href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/nominating_organization-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_election[Election]
        click hungarian_elections_election href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/election-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_district_hierarchy[District Hierarchy]
        click hungarian_elections_district_hierarchy href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/district_hierarchy-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_geographical_unit[Geographical Unit]
        click hungarian_elections_geographical_unit href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/geographical_unit-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_party[Party]
        click hungarian_elections_party href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/party-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_election_precinct[Election Precinct]
        click hungarian_elections_election_precinct href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/election_precinct-profile.html" "Profile"
        
        hungarian_elections([Hungarian Elections]) --- hungarian_elections_vote_record[Vote Record]
        click hungarian_elections_vote_record href "https://s3.eu-de.cloud-object-storage.appdomain.cloud/sscub-public-explorer-tutorial/hungarian_elections/vote_record-profile.html" "Profile"
        
```