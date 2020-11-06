---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azureatalakestorechilditemproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreChildItemProperties.md
ms.openlocfilehash: faaf8a0c614a1243a3e3812cd0b6e1202cc7e75b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580148"
---
# <span data-ttu-id="f94d5-101">Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="f94d5-101">Export-AzureRmDataLakeStoreChildItemProperties</span></span>

## <span data-ttu-id="f94d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f94d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f94d5-103">Exporterar egenskaperna (disk användning och ACL) för hela trädet från den angivna sökvägen till en Ouput-sökväg</span><span class="sxs-lookup"><span data-stu-id="f94d5-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a ouput path</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f94d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f94d5-104">SYNTAX</span></span>

### <span data-ttu-id="f94d5-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="f94d5-105">GetDiskUsage</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f94d5-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="f94d5-106">GetAllProperties</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f94d5-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="f94d5-107">GetAclDump</span></span>
```
Export-AzureRmDataLakeStoreChildItemProperties [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f94d5-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f94d5-108">DESCRIPTION</span></span>
<span data-ttu-id="f94d5-109">**Exportera-AzureRmDataLakeStoreChildItemProperties** används för att rapportera ADLS för användning eller/och ACL för den angivna katalogen och under kataloger och filer.</span><span class="sxs-lookup"><span data-stu-id="f94d5-109">The **Export-AzureRmDataLakeStoreChildItemProperties** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="f94d5-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f94d5-110">EXAMPLES</span></span>

### <span data-ttu-id="f94d5-111">Exempel 1: få disk användning och ACL-användning för alla under kataloger och filer</span><span class="sxs-lookup"><span data-stu-id="f94d5-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="f94d5-112">Få disk användning och ACL-användning för alla under kataloger och filer under/a.</span><span class="sxs-lookup"><span data-stu-id="f94d5-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="f94d5-113">IncludeFile säkerställer att användningen rapporteras för filer också</span><span class="sxs-lookup"><span data-stu-id="f94d5-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="f94d5-114">Exempel 2: Hämta ACL-användning för alla under kataloger och filer med den enhetliga åtkomst kontrol listan dold</span><span class="sxs-lookup"><span data-stu-id="f94d5-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzureRmDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzureRmDataLakeStoreChildItemProperties -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="f94d5-115">Hämta ACL-användning för alla under kataloger och filer under/a.</span><span class="sxs-lookup"><span data-stu-id="f94d5-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="f94d5-116">IncludeFile säkerställer att användningen rapporteras för filer också.</span><span class="sxs-lookup"><span data-stu-id="f94d5-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="f94d5-117">HideconsistentAcl i det här fallet visas ACL för/a, inte till barn eftersom alla underordnade har samma ACL som/a.</span><span class="sxs-lookup"><span data-stu-id="f94d5-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="f94d5-118">Den här flaggan hoppar över ACL-Ouput för under träd om alla dess åtkomst kontrol listor är samma som roten.</span><span class="sxs-lookup"><span data-stu-id="f94d5-118">This flag skips the acl ouput of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="f94d5-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f94d5-119">PARAMETERS</span></span>

### <span data-ttu-id="f94d5-120">-Konto</span><span class="sxs-lookup"><span data-stu-id="f94d5-120">-Account</span></span>
<span data-ttu-id="f94d5-121">Data Lake Store-kontot för att köra filesystem-åtgärden i</span><span class="sxs-lookup"><span data-stu-id="f94d5-121">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-122">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="f94d5-122">-Concurrency</span></span>
<span data-ttu-id="f94d5-123">Anger antalet filer/kataloger som har bearbetats parallellt.</span><span class="sxs-lookup"><span data-stu-id="f94d5-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="f94d5-124">Standard beräknas som en bästa ansträngning baserat på systemets specifikation.</span><span class="sxs-lookup"><span data-stu-id="f94d5-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f94d5-125">-DefaultProfile</span></span>
<span data-ttu-id="f94d5-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f94d5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="f94d5-127">-GetAcl</span></span>
<span data-ttu-id="f94d5-128">Hämtar åtkomst kontroll filen från rot Sök vägen</span><span class="sxs-lookup"><span data-stu-id="f94d5-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="f94d5-129">-GetDiskUsage</span></span>
<span data-ttu-id="f94d5-130">Hämtar disk användning från rot Sök vägen</span><span class="sxs-lookup"><span data-stu-id="f94d5-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="f94d5-131">-HideConsistentAcl</span></span>
<span data-ttu-id="f94d5-132">Visa inte katalog under träd om åtkomst kontrol listorna är identiska i hela under trädet.</span><span class="sxs-lookup"><span data-stu-id="f94d5-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="f94d5-133">Det gör det enklare att bara se vilka Sök vägar som är olika. Om till exempel alla filer och mappar under/a/b är desamma, ska du inte Visa subtreeunder/a/b och bara utskrivbar/a/b med "true" i den enhetliga ACL: en columnCannot ställs in om IncludeFiles inte är inställt, eftersom konsekvent ACL inte kan identifieras utan att hämta ACL för filerna.</span><span class="sxs-lookup"><span data-stu-id="f94d5-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="f94d5-134">-IncludeFile</span></span>
<span data-ttu-id="f94d5-135">Visa statistik på filnivå (standard är att visa endast information på katalog nivå)</span><span class="sxs-lookup"><span data-stu-id="f94d5-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="f94d5-136">-MaximumDepth</span></span>
<span data-ttu-id="f94d5-137">Maximalt djup från den rot katalog där disk användning eller ACL visas</span><span class="sxs-lookup"><span data-stu-id="f94d5-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="f94d5-138">-OutputPath</span></span>
<span data-ttu-id="f94d5-139">Sökvägen till utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="f94d5-139">Path to output file.</span></span> <span data-ttu-id="f94d5-140">Kan vara en lokal sökväg eller ADL sökväg.</span><span class="sxs-lookup"><span data-stu-id="f94d5-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="f94d5-141">Den är som standard lokal.</span><span class="sxs-lookup"><span data-stu-id="f94d5-141">By default it is local.</span></span> <span data-ttu-id="f94d5-142">Om SaveToAdl är pecified är det en ADL sökväg till samma konto</span><span class="sxs-lookup"><span data-stu-id="f94d5-142">If SaveToAdl is pecified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f94d5-143">-PassThru</span></span>
<span data-ttu-id="f94d5-144">Anger att ett booleskt svar ska returneras och anger resultatet av Delete-åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f94d5-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-145">-Path</span><span class="sxs-lookup"><span data-stu-id="f94d5-145">-Path</span></span>
<span data-ttu-id="f94d5-146">Sökvägen för det data Lake-konto som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="f94d5-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="f94d5-147">Kan vara en fil eller mapp i formatet '/Folder/file.txt ', där "/" efter DNS anger fil systemets rot.</span><span class="sxs-lookup"><span data-stu-id="f94d5-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="f94d5-148">-SaveToAdl</span></span>
<span data-ttu-id="f94d5-149">Om du har godkänt den sparas dumpfilen i ADL.</span><span class="sxs-lookup"><span data-stu-id="f94d5-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="f94d5-150">DumpFile få vara en ADL-bana i det fallet</span><span class="sxs-lookup"><span data-stu-id="f94d5-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f94d5-151">-Confirm</span></span>
<span data-ttu-id="f94d5-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f94d5-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f94d5-153">-WhatIf</span></span>
<span data-ttu-id="f94d5-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f94d5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f94d5-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f94d5-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f94d5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f94d5-156">CommonParameters</span></span>
<span data-ttu-id="f94d5-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f94d5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f94d5-158">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f94d5-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f94d5-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f94d5-159">INPUTS</span></span>

### <span data-ttu-id="f94d5-160">System. String</span><span class="sxs-lookup"><span data-stu-id="f94d5-160">System.String</span></span>

### <span data-ttu-id="f94d5-161">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="f94d5-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f94d5-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f94d5-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f94d5-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f94d5-163">System.Int32</span></span>

## <span data-ttu-id="f94d5-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f94d5-164">OUTPUTS</span></span>

### <span data-ttu-id="f94d5-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f94d5-165">System.Boolean</span></span>

## <span data-ttu-id="f94d5-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f94d5-166">NOTES</span></span>

## <span data-ttu-id="f94d5-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f94d5-167">RELATED LINKS</span></span>
