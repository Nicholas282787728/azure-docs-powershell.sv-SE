---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25091f0cb439e0447d19b534d59a0084a5b05c6e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94099871"
---
# <span data-ttu-id="48e5d-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="48e5d-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="48e5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="48e5d-103">Returnerar listan med konfigurationer för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="48e5d-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="48e5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48e5d-104">SYNTAX</span></span>

### <span data-ttu-id="48e5d-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="48e5d-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="48e5d-106">Lära</span><span class="sxs-lookup"><span data-stu-id="48e5d-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="48e5d-107">ID</span><span class="sxs-lookup"><span data-stu-id="48e5d-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="48e5d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48e5d-108">DESCRIPTION</span></span>
<span data-ttu-id="48e5d-109">Returnerar listan med konfigurationer för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="48e5d-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="48e5d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48e5d-110">EXAMPLES</span></span>

### <span data-ttu-id="48e5d-111">--------------------------EXEMPEL 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="48e5d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="48e5d-112">Skaffa Azure Stack backup-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="48e5d-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="48e5d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48e5d-113">PARAMETERS</span></span>

### <span data-ttu-id="48e5d-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="48e5d-114">-Location</span></span>
<span data-ttu-id="48e5d-115">Plats för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="48e5d-115">Backup location.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e5d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e5d-116">-ResourceGroupName</span></span>
<span data-ttu-id="48e5d-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="48e5d-117">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e5d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48e5d-118">-ResourceId</span></span>
<span data-ttu-id="48e5d-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="48e5d-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48e5d-120">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="48e5d-120">-Skip</span></span>
<span data-ttu-id="48e5d-121">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="48e5d-121">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e5d-122">-Överst</span><span class="sxs-lookup"><span data-stu-id="48e5d-122">-Top</span></span>
<span data-ttu-id="48e5d-123">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="48e5d-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="48e5d-124">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="48e5d-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e5d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e5d-125">CommonParameters</span></span>
<span data-ttu-id="48e5d-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48e5d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e5d-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e5d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e5d-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48e5d-128">INPUTS</span></span>

## <span data-ttu-id="48e5d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48e5d-129">OUTPUTS</span></span>

### <span data-ttu-id="48e5d-130">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="48e5d-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="48e5d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48e5d-131">NOTES</span></span>

## <span data-ttu-id="48e5d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48e5d-132">RELATED LINKS</span></span>

