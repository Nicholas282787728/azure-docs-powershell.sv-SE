---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090876"
---
# <span data-ttu-id="d3c1c-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d3c1c-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="d3c1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="d3c1c-103">Skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="d3c1c-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="d3c1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3c1c-104">SYNTAX</span></span>

### <span data-ttu-id="d3c1c-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="d3c1c-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3c1c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d3c1c-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3c1c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3c1c-107">DESCRIPTION</span></span>
<span data-ttu-id="d3c1c-108">Cmdleten **New-AzRmStorageContainer** skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="d3c1c-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="d3c1c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3c1c-109">EXAMPLES</span></span>

### <span data-ttu-id="d3c1c-110">Exempel 1: skapa en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata</span><span class="sxs-lookup"><span data-stu-id="d3c1c-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="d3c1c-111">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="d3c1c-112">Exempel 2: skapa en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som BLOB</span><span class="sxs-lookup"><span data-stu-id="d3c1c-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="d3c1c-113">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som blob.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="d3c1c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3c1c-114">PARAMETERS</span></span>

### <span data-ttu-id="d3c1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3c1c-115">-DefaultProfile</span></span>
<span data-ttu-id="d3c1c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3c1c-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d3c1c-117">-Metadata</span></span>
<span data-ttu-id="d3c1c-118">Metadata för behållare</span><span class="sxs-lookup"><span data-stu-id="d3c1c-118">Container Metadata</span></span>

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

### <span data-ttu-id="d3c1c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3c1c-119">-Name</span></span>
<span data-ttu-id="d3c1c-120">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="d3c1c-120">Container Name</span></span>

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

### <span data-ttu-id="d3c1c-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="d3c1c-121">-PublicAccess</span></span>
<span data-ttu-id="d3c1c-122">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="d3c1c-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="d3c1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3c1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3c1c-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="d3c1c-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3c1c-125">-StorageAccount</span></span>
<span data-ttu-id="d3c1c-126">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="d3c1c-126">Storage account object</span></span>

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

### <span data-ttu-id="d3c1c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d3c1c-127">-StorageAccountName</span></span>
<span data-ttu-id="d3c1c-128">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="d3c1c-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3c1c-129">-Confirm</span></span>
<span data-ttu-id="d3c1c-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3c1c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3c1c-131">-WhatIf</span></span>
<span data-ttu-id="d3c1c-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3c1c-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3c1c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3c1c-134">CommonParameters</span></span>
<span data-ttu-id="d3c1c-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3c1c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3c1c-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3c1c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3c1c-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3c1c-137">INPUTS</span></span>

### <span data-ttu-id="d3c1c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d3c1c-138">System.String</span></span>

### <span data-ttu-id="d3c1c-139">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3c1c-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d3c1c-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3c1c-140">OUTPUTS</span></span>

### <span data-ttu-id="d3c1c-141">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d3c1c-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d3c1c-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3c1c-142">NOTES</span></span>

## <span data-ttu-id="d3c1c-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3c1c-143">RELATED LINKS</span></span>
