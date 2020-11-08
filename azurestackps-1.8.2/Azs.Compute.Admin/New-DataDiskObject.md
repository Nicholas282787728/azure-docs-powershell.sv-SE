---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37d41ae2ec772cc755436bc01c3c4009c9c30f5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94100017"
---
# <span data-ttu-id="864dd-101">New-DataDiskObject</span><span class="sxs-lookup"><span data-stu-id="864dd-101">New-DataDiskObject</span></span>

## <span data-ttu-id="864dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="864dd-102">SYNOPSIS</span></span>
<span data-ttu-id="864dd-103">Skapar en data disk som används för att skapa en ny plattform för virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="864dd-103">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

## <span data-ttu-id="864dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="864dd-104">SYNTAX</span></span>

```
New-DataDiskObject [[-Lun] <Int32>] [[-Uri] <String>] [<CommonParameters>]
```

## <span data-ttu-id="864dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="864dd-105">DESCRIPTION</span></span>
<span data-ttu-id="864dd-106">Skapar ett objekt med information om en data disk.</span><span class="sxs-lookup"><span data-stu-id="864dd-106">Creates an object holding information about a data disk.</span></span>

## <span data-ttu-id="864dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="864dd-107">EXAMPLES</span></span>

### <span data-ttu-id="864dd-108">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="864dd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-DataDiskObject -Lun 5 -URI test.blob.windows.net/disks/datadisk5.vhd
```

<span data-ttu-id="864dd-109">Skapa ett nytt data objekt.</span><span class="sxs-lookup"><span data-stu-id="864dd-109">Create a new data disk object.</span></span>

## <span data-ttu-id="864dd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="864dd-110">PARAMETERS</span></span>

### <span data-ttu-id="864dd-111">-LUN</span><span class="sxs-lookup"><span data-stu-id="864dd-111">-Lun</span></span>
<span data-ttu-id="864dd-112">Logisk enhets nummer.</span><span class="sxs-lookup"><span data-stu-id="864dd-112">Logical unit number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="864dd-113">-URI</span><span class="sxs-lookup"><span data-stu-id="864dd-113">-Uri</span></span>
<span data-ttu-id="864dd-114">Plats för disk mal len.</span><span class="sxs-lookup"><span data-stu-id="864dd-114">Location of the disk template.</span></span>

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

### <span data-ttu-id="864dd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864dd-115">CommonParameters</span></span>
<span data-ttu-id="864dd-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="864dd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864dd-117">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="864dd-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864dd-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="864dd-118">INPUTS</span></span>

## <span data-ttu-id="864dd-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="864dd-119">OUTPUTS</span></span>

## <span data-ttu-id="864dd-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="864dd-120">NOTES</span></span>

## <span data-ttu-id="864dd-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="864dd-121">RELATED LINKS</span></span>

