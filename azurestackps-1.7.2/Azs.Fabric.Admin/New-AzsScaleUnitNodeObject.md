---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920845"
---
# <span data-ttu-id="ac97c-101">New-AzsScaleUnitNodeObject</span><span class="sxs-lookup"><span data-stu-id="ac97c-101">New-AzsScaleUnitNodeObject</span></span>

## <span data-ttu-id="ac97c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac97c-102">SYNOPSIS</span></span>
<span data-ttu-id="ac97c-103">Ange data som används för att lägga till en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="ac97c-103">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="ac97c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac97c-104">SYNTAX</span></span>

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ac97c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac97c-105">DESCRIPTION</span></span>
<span data-ttu-id="ac97c-106">Ange data som används för att lägga till en nod för skalnings enhet.</span><span class="sxs-lookup"><span data-stu-id="ac97c-106">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="ac97c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac97c-107">EXAMPLES</span></span>

### <span data-ttu-id="ac97c-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ac97c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

<span data-ttu-id="ac97c-109">Skapa ett nytt nod-objekt.</span><span class="sxs-lookup"><span data-stu-id="ac97c-109">Create a new node object.</span></span>

## <span data-ttu-id="ac97c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac97c-110">PARAMETERS</span></span>

### <span data-ttu-id="ac97c-111">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="ac97c-111">-BMCIPv4Address</span></span>
<span data-ttu-id="ac97c-112">BMC-adress för den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="ac97c-112">Bmc address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac97c-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ac97c-113">-ComputerName</span></span>
<span data-ttu-id="ac97c-114">Dator namnet på den fysiska datorn.</span><span class="sxs-lookup"><span data-stu-id="ac97c-114">Computer name of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac97c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac97c-115">CommonParameters</span></span>
<span data-ttu-id="ac97c-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac97c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac97c-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac97c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac97c-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac97c-118">INPUTS</span></span>

## <span data-ttu-id="ac97c-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac97c-119">OUTPUTS</span></span>

## <span data-ttu-id="ac97c-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac97c-120">NOTES</span></span>

## <span data-ttu-id="ac97c-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac97c-121">RELATED LINKS</span></span>
