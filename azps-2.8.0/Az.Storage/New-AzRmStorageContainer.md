---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: efbdcc79bed4b7dd3dcca40f87db7fcef668405a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920892"
---
# <span data-ttu-id="ed86d-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ed86d-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="ed86d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed86d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed86d-103">Skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="ed86d-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="ed86d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed86d-104">SYNTAX</span></span>

### <span data-ttu-id="ed86d-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="ed86d-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed86d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ed86d-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed86d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed86d-107">DESCRIPTION</span></span>
<span data-ttu-id="ed86d-108">Cmdleten **New-AzRmStorageContainer** skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="ed86d-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="ed86d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed86d-109">EXAMPLES</span></span>

### <span data-ttu-id="ed86d-110">Exempel 1: skapa en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata</span><span class="sxs-lookup"><span data-stu-id="ed86d-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="ed86d-111">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata.</span><span class="sxs-lookup"><span data-stu-id="ed86d-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="ed86d-112">Exempel 2: skapa en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som BLOB</span><span class="sxs-lookup"><span data-stu-id="ed86d-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="ed86d-113">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som blob.</span><span class="sxs-lookup"><span data-stu-id="ed86d-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="ed86d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed86d-114">PARAMETERS</span></span>

### <span data-ttu-id="ed86d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed86d-115">-DefaultProfile</span></span>
<span data-ttu-id="ed86d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed86d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed86d-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ed86d-117">-Metadata</span></span>
<span data-ttu-id="ed86d-118">Metadata för behållare</span><span class="sxs-lookup"><span data-stu-id="ed86d-118">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed86d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="ed86d-119">-Name</span></span>
<span data-ttu-id="ed86d-120">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="ed86d-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed86d-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="ed86d-121">-PublicAccess</span></span>
<span data-ttu-id="ed86d-122">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="ed86d-122">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed86d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed86d-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed86d-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ed86d-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed86d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed86d-125">-StorageAccount</span></span>
<span data-ttu-id="ed86d-126">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="ed86d-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed86d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ed86d-127">-StorageAccountName</span></span>
<span data-ttu-id="ed86d-128">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="ed86d-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed86d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ed86d-129">-Confirm</span></span>
<span data-ttu-id="ed86d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ed86d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed86d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed86d-131">-WhatIf</span></span>
<span data-ttu-id="ed86d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ed86d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed86d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ed86d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed86d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed86d-134">CommonParameters</span></span>
<span data-ttu-id="ed86d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed86d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed86d-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed86d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed86d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed86d-137">INPUTS</span></span>

### <span data-ttu-id="ed86d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ed86d-138">System.String</span></span>

### <span data-ttu-id="ed86d-139">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed86d-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ed86d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed86d-140">OUTPUTS</span></span>

### <span data-ttu-id="ed86d-141">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="ed86d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="ed86d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed86d-142">NOTES</span></span>

## <span data-ttu-id="ed86d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed86d-143">RELATED LINKS</span></span>
