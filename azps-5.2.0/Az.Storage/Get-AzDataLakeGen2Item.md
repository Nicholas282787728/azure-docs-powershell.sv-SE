---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388932"
---
# <span data-ttu-id="451e5-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="451e5-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="451e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="451e5-102">SYNOPSIS</span></span>
<span data-ttu-id="451e5-103">Hämtar information om en fil eller katalog i ett fil system.</span><span class="sxs-lookup"><span data-stu-id="451e5-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="451e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="451e5-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="451e5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="451e5-105">DESCRIPTION</span></span>
<span data-ttu-id="451e5-106">Cmdleten **Get-AzDataLakeGen2Item** hämtar information om en fil eller katalog i ett fil system i ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="451e5-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="451e5-107">Denna cmdlet fungerar bara om hierarkisk namnrymd är aktiverat för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="451e5-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="451e5-108">Den här typen av konto kan skapas med kör "New-AzStorageAccount"-cmdlet med "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="451e5-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="451e5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="451e5-109">EXAMPLES</span></span>

### <span data-ttu-id="451e5-110">Exempel 1: Hämta en katalog från ett filesystem och Visa informationen</span><span class="sxs-lookup"><span data-stu-id="451e5-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="451e5-111">Det här kommandot får en katalog från ett filesystem och visar informationen.</span><span class="sxs-lookup"><span data-stu-id="451e5-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="451e5-112">Exempel 2: Hämta en fil från ett filesystem</span><span class="sxs-lookup"><span data-stu-id="451e5-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="451e5-113">Det här kommandot får information om en fil från ett fil system.</span><span class="sxs-lookup"><span data-stu-id="451e5-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="451e5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="451e5-114">PARAMETERS</span></span>

### <span data-ttu-id="451e5-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="451e5-115">-Context</span></span>
<span data-ttu-id="451e5-116">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="451e5-116">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="451e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451e5-117">-DefaultProfile</span></span>
<span data-ttu-id="451e5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="451e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="451e5-119">-Fil system</span><span class="sxs-lookup"><span data-stu-id="451e5-119">-FileSystem</span></span>
<span data-ttu-id="451e5-120">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="451e5-120">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="451e5-121">-Path</span><span class="sxs-lookup"><span data-stu-id="451e5-121">-Path</span></span>
<span data-ttu-id="451e5-122">Sökvägen i angivet filesystem som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="451e5-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="451e5-123">Kan vara en fil eller katalog i formatet ' katalog/file.txt ' eller ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="451e5-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="451e5-124">Inte ange den här parametern för att hämta fil systemets rot Katalog.</span><span class="sxs-lookup"><span data-stu-id="451e5-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="451e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451e5-125">CommonParameters</span></span>
<span data-ttu-id="451e5-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="451e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451e5-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="451e5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451e5-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="451e5-128">INPUTS</span></span>

### <span data-ttu-id="451e5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="451e5-129">System.String</span></span>

### <span data-ttu-id="451e5-130">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="451e5-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="451e5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="451e5-131">OUTPUTS</span></span>

### <span data-ttu-id="451e5-132">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="451e5-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="451e5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="451e5-133">NOTES</span></span>

## <span data-ttu-id="451e5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="451e5-134">RELATED LINKS</span></span>
