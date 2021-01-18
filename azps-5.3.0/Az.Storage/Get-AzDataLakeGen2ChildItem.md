---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520327"
---
# <span data-ttu-id="d5148-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="d5148-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="d5148-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d5148-102">SYNOPSIS</span></span>
<span data-ttu-id="d5148-103">Visar under kataloger och filer från en katalog eller fil Systems rot.</span><span class="sxs-lookup"><span data-stu-id="d5148-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="d5148-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d5148-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5148-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d5148-105">DESCRIPTION</span></span>
<span data-ttu-id="d5148-106">Cmdleten **Get-AzDataLakeGen2ChildItem** visar under kataloger och filer i en katalog eller fil system i ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="d5148-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="d5148-107">Denna cmdlet fungerar bara om hierarkisk namnrymd är aktiverat för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d5148-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="d5148-108">Den här typen av konto kan skapas med kör "New-AzStorageAccount"-cmdlet med "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="d5148-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="d5148-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d5148-109">EXAMPLES</span></span>

### <span data-ttu-id="d5148-110">Exempel 1: lista direkta under objekt från ett filesystem</span><span class="sxs-lookup"><span data-stu-id="d5148-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="d5148-111">Det här kommandot listar direkt under objekt från ett filesystem</span><span class="sxs-lookup"><span data-stu-id="d5148-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="d5148-112">Exempel 2: lista rekursivt från en katalog och Fetch-egenskaper/ACL</span><span class="sxs-lookup"><span data-stu-id="d5148-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="d5148-113">Det här kommandot listar direkt under objekt från ett filesystem</span><span class="sxs-lookup"><span data-stu-id="d5148-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="d5148-114">Exempel 3: list objekt rekursivt från ett filesystem i flera batchar</span><span class="sxs-lookup"><span data-stu-id="d5148-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="d5148-115">I det här exemplet används parametrarna *MaxCount* och *ContinuationToken* för att lista objekt rekursivt från ett filesystem i flera batchar.</span><span class="sxs-lookup"><span data-stu-id="d5148-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="d5148-116">De första fyra kommandona tilldelar värden till variabler som ska användas i exemplet.</span><span class="sxs-lookup"><span data-stu-id="d5148-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="d5148-117">Det femte kommandot anger en **do-while-** sats som använder cmdleten **Get-AzDataLakeGen2ChildItem** för List objekt.</span><span class="sxs-lookup"><span data-stu-id="d5148-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="d5148-118">Uttrycket innehåller det tilläggs token som lagras i $Token variabeln.</span><span class="sxs-lookup"><span data-stu-id="d5148-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="d5148-119">$Token ändrar värde när slingan körs.</span><span class="sxs-lookup"><span data-stu-id="d5148-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="d5148-120">Det sista kommandot använder kommandot **ECHO** för att visa summan.</span><span class="sxs-lookup"><span data-stu-id="d5148-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="d5148-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d5148-121">PARAMETERS</span></span>

### <span data-ttu-id="d5148-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5148-122">-AsJob</span></span>
<span data-ttu-id="d5148-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d5148-123">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5148-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d5148-124">-Context</span></span>
<span data-ttu-id="d5148-125">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="d5148-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d5148-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="d5148-126">-ContinuationToken</span></span>
<span data-ttu-id="d5148-127">Fortsättnings-token.</span><span class="sxs-lookup"><span data-stu-id="d5148-127">Continuation Token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5148-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5148-128">-DefaultProfile</span></span>
<span data-ttu-id="d5148-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d5148-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5148-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="d5148-130">-FetchProperty</span></span>
<span data-ttu-id="d5148-131">Hämta datalake objekt egenskaper och åtkomst kontrol lista.</span><span class="sxs-lookup"><span data-stu-id="d5148-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5148-132">-Fil system</span><span class="sxs-lookup"><span data-stu-id="d5148-132">-FileSystem</span></span>
<span data-ttu-id="d5148-133">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="d5148-133">FileSystem name</span></span>

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

### <span data-ttu-id="d5148-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d5148-134">-MaxCount</span></span>
<span data-ttu-id="d5148-135">Det högsta antalet BLOB-nummer som kan returneras.</span><span class="sxs-lookup"><span data-stu-id="d5148-135">The max count of the blobs that can return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5148-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d5148-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="d5148-137">Om du speicify den här parametern omvandlas de användar-ID-värden som anges i fälten owner och Group för varje List post från objekt-ID: n för Azure Active Directory till användarens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="d5148-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="d5148-138">Om du inte speicify den här parametern returneras värdena som Azure Active Directory-objekt-ID.</span><span class="sxs-lookup"><span data-stu-id="d5148-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="d5148-139">Observera att grupp-och program objekt-ID inte översätts eftersom de inte har unika namn.</span><span class="sxs-lookup"><span data-stu-id="d5148-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5148-140">-Path</span><span class="sxs-lookup"><span data-stu-id="d5148-140">-Path</span></span>
<span data-ttu-id="d5148-141">Sökvägen i angivet filesystem som ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="d5148-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="d5148-142">Ska vara en katalog, i formatet ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="d5148-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5148-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="d5148-143">-Recurse</span></span>
<span data-ttu-id="d5148-144">Anger om det underordnade objektet ska hämtas rekursivt.</span><span class="sxs-lookup"><span data-stu-id="d5148-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="d5148-145">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="d5148-145">The default is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5148-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5148-146">CommonParameters</span></span>
<span data-ttu-id="d5148-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5148-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5148-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5148-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5148-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d5148-149">INPUTS</span></span>

### <span data-ttu-id="d5148-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d5148-150">System.String</span></span>

### <span data-ttu-id="d5148-151">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d5148-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d5148-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d5148-152">OUTPUTS</span></span>

### <span data-ttu-id="d5148-153">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d5148-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="d5148-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d5148-154">NOTES</span></span>

## <span data-ttu-id="d5148-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d5148-155">RELATED LINKS</span></span>
