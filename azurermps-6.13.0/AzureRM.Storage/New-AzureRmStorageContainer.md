---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573859"
---
# <span data-ttu-id="2e82e-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2e82e-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="2e82e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e82e-102">SYNOPSIS</span></span>
<span data-ttu-id="2e82e-103">Skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="2e82e-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e82e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e82e-104">SYNTAX</span></span>

### <span data-ttu-id="2e82e-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="2e82e-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e82e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2e82e-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e82e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e82e-107">DESCRIPTION</span></span>
<span data-ttu-id="2e82e-108">Cmdleten **New-AzureRmStorageContainer** skapar en lagrings-BLOB-behållare</span><span class="sxs-lookup"><span data-stu-id="2e82e-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="2e82e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e82e-109">EXAMPLES</span></span>

### <span data-ttu-id="2e82e-110">Exempel 1: skapa en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata</span><span class="sxs-lookup"><span data-stu-id="2e82e-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="2e82e-111">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto namn och container namn, med metadata.</span><span class="sxs-lookup"><span data-stu-id="2e82e-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="2e82e-112">Exempel 2: skapa en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som BLOB</span><span class="sxs-lookup"><span data-stu-id="2e82e-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="2e82e-113">Det här kommandot skapar en lagrings-BLOB-behållare med lagrings konto objekt och container namn, med offentlig åtkomst som blob.</span><span class="sxs-lookup"><span data-stu-id="2e82e-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="2e82e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e82e-114">PARAMETERS</span></span>

### <span data-ttu-id="2e82e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e82e-115">-DefaultProfile</span></span>
<span data-ttu-id="2e82e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e82e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="2e82e-117">-Metadata</span></span>
<span data-ttu-id="2e82e-118">Metadata för behållare</span><span class="sxs-lookup"><span data-stu-id="2e82e-118">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e82e-119">-Name</span></span>
<span data-ttu-id="2e82e-120">Behållare namn</span><span class="sxs-lookup"><span data-stu-id="2e82e-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="2e82e-121">-PublicAccess</span></span>
<span data-ttu-id="2e82e-122">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="2e82e-122">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e82e-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e82e-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="2e82e-124">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2e82e-125">-StorageAccount</span></span>
<span data-ttu-id="2e82e-126">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="2e82e-126">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2e82e-127">-StorageAccountName</span></span>
<span data-ttu-id="2e82e-128">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="2e82e-128">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e82e-129">-Confirm</span></span>
<span data-ttu-id="2e82e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e82e-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e82e-131">-WhatIf</span></span>
<span data-ttu-id="2e82e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2e82e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e82e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2e82e-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e82e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e82e-134">CommonParameters</span></span>
<span data-ttu-id="2e82e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e82e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e82e-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e82e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e82e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e82e-137">INPUTS</span></span>

### <span data-ttu-id="2e82e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2e82e-138">System.String</span></span>

## <span data-ttu-id="2e82e-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e82e-139">OUTPUTS</span></span>

### <span data-ttu-id="2e82e-140">Microsoft. Azure. commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="2e82e-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="2e82e-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e82e-141">NOTES</span></span>

## <span data-ttu-id="2e82e-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e82e-142">RELATED LINKS</span></span>

