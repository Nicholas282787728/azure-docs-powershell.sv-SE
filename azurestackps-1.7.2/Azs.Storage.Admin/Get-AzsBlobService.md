---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d9ff0746de44d2e5c3c67ea95b66dd3bd3902ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919858"
---
# <span data-ttu-id="ef166-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="ef166-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="ef166-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef166-102">SYNOPSIS</span></span>
<span data-ttu-id="ef166-103">Returnerar Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ef166-103">Returns the blob service.</span></span>

## <span data-ttu-id="ef166-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef166-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef166-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef166-105">DESCRIPTION</span></span>
<span data-ttu-id="ef166-106">Returnerar Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ef166-106">Returns the blob service.</span></span>

## <span data-ttu-id="ef166-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef166-107">EXAMPLES</span></span>

### <span data-ttu-id="ef166-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ef166-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="ef166-109">Skaffa Blob-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ef166-109">Get the blob service.</span></span>

## <span data-ttu-id="ef166-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef166-110">PARAMETERS</span></span>

### <span data-ttu-id="ef166-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="ef166-111">-FarmName</span></span>
<span data-ttu-id="ef166-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="ef166-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef166-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef166-113">-ResourceGroupName</span></span>
<span data-ttu-id="ef166-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="ef166-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef166-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef166-115">CommonParameters</span></span>
<span data-ttu-id="ef166-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef166-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef166-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef166-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef166-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef166-118">INPUTS</span></span>

## <span data-ttu-id="ef166-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef166-119">OUTPUTS</span></span>

### <span data-ttu-id="ef166-120">Microsoft. AzureStack. Management. Storage. admin. Models. BlobService</span><span class="sxs-lookup"><span data-stu-id="ef166-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="ef166-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef166-121">NOTES</span></span>

## <span data-ttu-id="ef166-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef166-122">RELATED LINKS</span></span>
