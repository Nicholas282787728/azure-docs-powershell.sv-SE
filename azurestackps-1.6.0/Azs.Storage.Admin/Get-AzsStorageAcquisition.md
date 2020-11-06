---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3562b169211d4c3b1f87260be37a94f6de2e8b85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571871"
---
# <span data-ttu-id="70213-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="70213-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="70213-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70213-102">SYNOPSIS</span></span>
<span data-ttu-id="70213-103">Returnerar en lista över BLOB-Acquistions.</span><span class="sxs-lookup"><span data-stu-id="70213-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="70213-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70213-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="70213-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70213-105">DESCRIPTION</span></span>
<span data-ttu-id="70213-106">Returnerar en lista över BLOB-Acquistions.</span><span class="sxs-lookup"><span data-stu-id="70213-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="70213-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70213-107">EXAMPLES</span></span>

### <span data-ttu-id="70213-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="70213-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="70213-109">Hämta listan över BLOB-Acquistions.</span><span class="sxs-lookup"><span data-stu-id="70213-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="70213-110">--------------------------EXEMPEL 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="70213-110">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="70213-111">Hämta listan över BLOB-Acquistions.</span><span class="sxs-lookup"><span data-stu-id="70213-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="70213-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70213-112">PARAMETERS</span></span>

### <span data-ttu-id="70213-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="70213-113">-FarmName</span></span>
<span data-ttu-id="70213-114">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="70213-114">Farm Id.</span></span>

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

### <span data-ttu-id="70213-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="70213-115">-Filter</span></span>
<span data-ttu-id="70213-116">Filter sträng</span><span class="sxs-lookup"><span data-stu-id="70213-116">Filter string</span></span>

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

### <span data-ttu-id="70213-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70213-117">-ResourceGroupName</span></span>
<span data-ttu-id="70213-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="70213-118">Resource group name.</span></span>

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

### <span data-ttu-id="70213-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70213-119">CommonParameters</span></span>
<span data-ttu-id="70213-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70213-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70213-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70213-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70213-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70213-122">INPUTS</span></span>

## <span data-ttu-id="70213-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70213-123">OUTPUTS</span></span>

## <span data-ttu-id="70213-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70213-124">NOTES</span></span>

## <span data-ttu-id="70213-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70213-125">RELATED LINKS</span></span>

