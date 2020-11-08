---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103414"
---
# <span data-ttu-id="19004-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19004-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="19004-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19004-102">SYNOPSIS</span></span>
<span data-ttu-id="19004-103">Hämtar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="19004-103">Gets a Storage account.</span></span>

## <span data-ttu-id="19004-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19004-104">SYNTAX</span></span>

### <span data-ttu-id="19004-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="19004-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19004-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19004-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19004-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="19004-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19004-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19004-108">DESCRIPTION</span></span>
<span data-ttu-id="19004-109">Cmdleten **Get-AzStorageAccount** hämtar ett angivet lagrings konto eller alla lagrings konton i en resurs grupp eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="19004-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="19004-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19004-110">EXAMPLES</span></span>

### <span data-ttu-id="19004-111">Exempel 1: skaffa ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="19004-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="19004-112">Det här kommandot hämtar det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="19004-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="19004-113">Exempel 2: Hämta alla lagrings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="19004-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="19004-114">Det här kommandot får alla lagrings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="19004-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="19004-115">Exempel 3: Hämta alla lagrings konton i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="19004-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="19004-116">Det här kommandot får alla lagrings konton i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="19004-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="19004-117">Exempel 4: skaffa ett lagrings konto med sin BLOB Restore-status</span><span class="sxs-lookup"><span data-stu-id="19004-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="19004-118">Det här kommandot får ett lagrings konto med sin BLOB Restore-status och visar BLOB Restore-status.</span><span class="sxs-lookup"><span data-stu-id="19004-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="19004-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19004-119">PARAMETERS</span></span>

### <span data-ttu-id="19004-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19004-120">-AsJob</span></span>
<span data-ttu-id="19004-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="19004-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19004-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19004-122">-DefaultProfile</span></span>
<span data-ttu-id="19004-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19004-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19004-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="19004-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="19004-125">Hämta BlobRestoreStatus för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="19004-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19004-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="19004-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="19004-127">Hämta GeoReplicationStats för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="19004-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19004-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="19004-128">-Name</span></span>
<span data-ttu-id="19004-129">Anger namnet på det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="19004-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19004-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19004-130">-ResourceGroupName</span></span>
<span data-ttu-id="19004-131">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="19004-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19004-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19004-132">CommonParameters</span></span>
<span data-ttu-id="19004-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19004-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19004-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19004-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19004-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19004-135">INPUTS</span></span>

### <span data-ttu-id="19004-136">System. String</span><span class="sxs-lookup"><span data-stu-id="19004-136">System.String</span></span>

## <span data-ttu-id="19004-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19004-137">OUTPUTS</span></span>

### <span data-ttu-id="19004-138">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19004-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="19004-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19004-139">NOTES</span></span>

## <span data-ttu-id="19004-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19004-140">RELATED LINKS</span></span>

[<span data-ttu-id="19004-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19004-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="19004-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19004-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="19004-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19004-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


