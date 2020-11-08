---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 01b3c055873276a265859683e07cd9150ffedafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920906"
---
# <span data-ttu-id="1868e-101">Get-AzsTableService</span><span class="sxs-lookup"><span data-stu-id="1868e-101">Get-AzsTableService</span></span>

## <span data-ttu-id="1868e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1868e-102">SYNOPSIS</span></span>
<span data-ttu-id="1868e-103">Returnerar tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1868e-103">Returns the table service.</span></span>

## <span data-ttu-id="1868e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1868e-104">SYNTAX</span></span>

```
Get-AzsTableService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="1868e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1868e-105">DESCRIPTION</span></span>
<span data-ttu-id="1868e-106">Returnerar tabell tjänsten.</span><span class="sxs-lookup"><span data-stu-id="1868e-106">Returns the table service.</span></span>

## <span data-ttu-id="1868e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1868e-107">EXAMPLES</span></span>

### <span data-ttu-id="1868e-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1868e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="1868e-109">Skaffa tabellen service.</span><span class="sxs-lookup"><span data-stu-id="1868e-109">Get the table servie.</span></span>

## <span data-ttu-id="1868e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1868e-110">PARAMETERS</span></span>

### <span data-ttu-id="1868e-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="1868e-111">-FarmName</span></span>
<span data-ttu-id="1868e-112">Server grupp-ID.</span><span class="sxs-lookup"><span data-stu-id="1868e-112">Farm Id.</span></span>

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

### <span data-ttu-id="1868e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1868e-113">-ResourceGroupName</span></span>
<span data-ttu-id="1868e-114">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1868e-114">Resource group name.</span></span>

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

### <span data-ttu-id="1868e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1868e-115">CommonParameters</span></span>
<span data-ttu-id="1868e-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1868e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1868e-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1868e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1868e-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1868e-118">INPUTS</span></span>

## <span data-ttu-id="1868e-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1868e-119">OUTPUTS</span></span>

### <span data-ttu-id="1868e-120">Microsoft. AzureStack. Management. Storage. admin. Models. TableService</span><span class="sxs-lookup"><span data-stu-id="1868e-120">Microsoft.AzureStack.Management.Storage.Admin.Models.TableService</span></span>

## <span data-ttu-id="1868e-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1868e-121">NOTES</span></span>

## <span data-ttu-id="1868e-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1868e-122">RELATED LINKS</span></span>
