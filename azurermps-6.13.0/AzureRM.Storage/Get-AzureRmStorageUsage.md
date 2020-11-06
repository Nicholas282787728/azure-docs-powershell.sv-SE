---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578743"
---
# <span data-ttu-id="8ab48-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8ab48-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="8ab48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ab48-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab48-103">Hämtar lagrings resursanvändningen för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8ab48-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ab48-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ab48-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ab48-105">DESCRIPTION</span></span>
<span data-ttu-id="8ab48-106">Cmdleten **Get-AzureRmStorageUsage** hämtar resursanvändningen för Azure Storage för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8ab48-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="8ab48-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ab48-107">EXAMPLES</span></span>

### <span data-ttu-id="8ab48-108">Exempel 1: skaffa användning av lagrings resurser</span><span class="sxs-lookup"><span data-stu-id="8ab48-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="8ab48-109">Det här kommandot får användning av lagrings resurserna för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="8ab48-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="8ab48-110">Exempel 2: Hämta lagrings resurserna på den angivna platsen</span><span class="sxs-lookup"><span data-stu-id="8ab48-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="8ab48-111">Det här kommandot får lagrings resurserna på den angivna platsen under den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8ab48-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="8ab48-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ab48-112">PARAMETERS</span></span>

### <span data-ttu-id="8ab48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab48-113">-DefaultProfile</span></span>
<span data-ttu-id="8ab48-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ab48-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ab48-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="8ab48-115">-Location</span></span>
<span data-ttu-id="8ab48-116">Ange att du vill använda användning av lagrings resurser på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="8ab48-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="8ab48-117">Om inget anges får du lagrings resurser på alla platser under prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="8ab48-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab48-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab48-118">CommonParameters</span></span>
<span data-ttu-id="8ab48-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ab48-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab48-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ab48-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab48-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ab48-121">INPUTS</span></span>

### <span data-ttu-id="8ab48-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="8ab48-122">None</span></span>

## <span data-ttu-id="8ab48-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ab48-123">OUTPUTS</span></span>

### <span data-ttu-id="8ab48-124">Microsoft. Azure. commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="8ab48-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="8ab48-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ab48-125">NOTES</span></span>

## <span data-ttu-id="8ab48-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ab48-126">RELATED LINKS</span></span>

[<span data-ttu-id="8ab48-127">Azure Storage Manager-cmdletar</span><span class="sxs-lookup"><span data-stu-id="8ab48-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


