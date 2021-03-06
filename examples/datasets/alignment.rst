Example AlignmentSet XML::

  <?xml version="1.0" encoding="utf-8"?>
  <pbds:AlignmentSet 
      xmlns:pbbase="http://pacificbiosciences.com/PacBioBaseDataModel.xsd"  
      xmlns:pbsample="http://pacificbiosciences.com/PacBioSampleInfo.xsd" 
      xmlns:pbmeta="http://pacificbiosciences.com/PacBioCollectionMetadata.xsd" 
      xmlns:pbds="http://pacificbiosciences.com/PacBioDatasets.xsd" 
      xmlns="http://pacificbiosciences.com/PacBioDataModel.xsd" 
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://pacificbiosciences.com/PacBioDataModel.xsd"
      Tags="barcode moreTags mapping mytags" 
      UniqueId="b095d0a3-94b8-4918-b3af-a3f81bbe519c" 
      TimeStampedName="alignmentset_150304_231155"
      MetaType="PacBio.DataSet.AlignmentSet" 
      Name="Uber alignment set" 
      Version="2.3.0" 
      CreatedAt="2015-01-27T09:00:01">
      <pbbase:ExternalResources>
          <pbbase:ExternalResource 
              Name="First Alignments BAM" 
              Description="Points to an example Alignments BAM file." 
              UniqueId="b095d0a3-94b8-4918-b3af-a3f81bbe5293" 
              TimeStampedName="alignment_bam_150304_231155"
              MetaType="PacBio.AlignmentFile.AlignmentBamFile" 
              ResourceId="file:///mnt/path/to/alignments0.bam" Tags="Example">
              <pbbase:FileIndices>
                  <pbbase:FileIndex 
                      UniqueId="b095d0a3-94b8-4918-b3af-a3f81bbe5393" 
                      TimeStampedName="bam_index_150304_231155"
                      MetaType="PacBio.Index.PacBioIndex" 
                      ResourceId="file:///mnt/path/to/alignments0.pbi"/>
              </pbbase:FileIndices>
              <pbbase:ExternalResources>
                  <pbbase:ExternalResource 
                      Name="Reference used to produce BAM file" 
                      Description="Points to the reference used to generate the above BAM file." 
                      UniqueId="b095d0a3-94b8-4918-b3af-a3f81bbe5493" 
                      TimeStampedName="reference_fasta_150304_231155"
                      MetaType="PacBio.ReferenceFile.ReferenceFastaFile" 
                      ResourceId="file:///mnt/path/to/reference.fasta" Tags="Example">
                      <pbbase:FileIndices>
                          <pbbase:FileIndex 
                              UniqueId="b095d0a3-94b8-4918-b3af-a3f81bbe5593" 
                              TimeStampedName="sawriter_index_150304_231155"
                              MetaType="PacBio.Index.SaWriterIndex" 
                              ResourceId="file:///mnt/path/to/reference.fasta.sa"/>
                          <pbbase:FileIndex 
                              UniqueId="b095d0a3-94b8-4918-b3af-a3f81bbe5693" 
                              TimeStampedName="sam_index_150304_231155"
                              MetaType="PacBio.Index.SamIndex" 
                              ResourceId="file:///mnt/path/to/reference.fasta.fai"/>
                      </pbbase:FileIndices>
                  </pbbase:ExternalResource>
              </pbbase:ExternalResources>
          </pbbase:ExternalResource>
          <!-- Is this second BAM necessary? <pbbase:ExternalResource Name="Second Alignments BAM" Description="Points to another example Alignments BAM file, by relative path." MetaType="PacBio.AlignmentFile.AlignmentBamFile" ResourceId="file:./alignments1.bam" Tags="Example">
              <pbbase:FileIndices>
                  <pbbase:FileIndex MetaType="PacBio.Index.PacBioIndex" ResourceId="file:///mnt/path/to/alignments1.pbi"/>
              </pbbase:FileIndices>
          </pbbase:ExternalResource>-->
  
      </pbbase:ExternalResources>
  <!--  START use IDREF here for External Resources, or just duplicate them?  <pbds:DataSets>
          <pbds:DataSet 
              UniqueId="ab95d0a3-94b8-4918-b3af-a3f81bbe519c" 
              TimeStampedName="alignmentset_150304_231155"
              MetaType="PacBio.DataSet.AlignmentSet" 
              Version="2.3.0" 
              Name="HighQuality Read Alignments">
              <pbbase:ExternalResources>
                  <ExternalResource/>
              </pbbase:ExternalResources>
              <pbds:Filters> These Filters are in addition to those above. This provides a means to subset and label the parent DataSet further. 
                  <pbds:Filter>
                      <pbbase:Properties>
                          <pbbase:Property Name="rq" Value="0.85" Operator=">"/>
                      </pbbase:Properties>
                  </pbds:Filter>
              </pbds:Filters>
          </pbds:DataSet>
          <pbds:DataSet 
              UniqueId="ac95d0a3-94b8-4918-b3af-a3f81bbe519c" 
              TimeStampedName="alignmentset_150304_231155"
              MetaType="PacBio.DataSet.AlignmentSet" 
              Version="2.3.0" 
              Name="Alignments to chromosome 1">
              <pbbase:ExternalResources>
                  <ExternalResource/>
              </pbbase:ExternalResources>
              <pbds:Filters>
                  <pbds:Filter>
                      <pbbase:Properties>
                          <pbbase:Property Name="RNAME" Value="chr1" Operator="=="/>
                      </pbbase:Properties>
                  </pbds:Filter>
              </pbds:Filters>
          </pbds:DataSet>
      </pbds:DataSets>
      -->
      <pbds:DataSetMetadata>
          <pbds:TotalLength>50000</pbds:TotalLength>
          <pbds:NumRecords>5000</pbds:NumRecords>
          <pbds:Provenance CreatedBy="AnalysisJob">
              <pbds:ParentTool Name="pbalign" Version="0.1.0" Description="pbalign subreads.dataset.xml reference.dataset.xml"/>
          </pbds:Provenance>
      </pbds:DataSetMetadata>
  </pbds:AlignmentSet>
