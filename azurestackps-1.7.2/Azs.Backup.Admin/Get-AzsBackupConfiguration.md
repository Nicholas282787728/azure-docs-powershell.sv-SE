---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1f3a965d287aa266683636b4b17a8d8954cace8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93921071"
---
# <span data-ttu-id="ab404-101">Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab404-101">Get-AzsBackupConfiguration</span></span>

## <span data-ttu-id="ab404-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ab404-102">SYNOPSIS</span></span>
<span data-ttu-id="ab404-103">Returnerar listan med konfigurationer för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="ab404-103">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="ab404-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ab404-104">SYNTAX</span></span>

### <span data-ttu-id="ab404-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="ab404-105">List (Default)</span></span>
```
Get-AzsBackupConfiguration [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ab404-106">Lära</span><span class="sxs-lookup"><span data-stu-id="ab404-106">Get</span></span>
```
Get-AzsBackupConfiguration [[-Location] <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ab404-107">ID</span><span class="sxs-lookup"><span data-stu-id="ab404-107">ResourceId</span></span>
```
Get-AzsBackupConfiguration -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ab404-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ab404-108">DESCRIPTION</span></span>
<span data-ttu-id="ab404-109">Returnerar listan med konfigurationer för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="ab404-109">Returns the list of backup configurations.</span></span>

## <span data-ttu-id="ab404-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ab404-110">EXAMPLES</span></span>

### <span data-ttu-id="ab404-111">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="ab404-111">EXAMPLE 1</span></span>
```
Get-AzsBackupConfiguration
```

<span data-ttu-id="ab404-112">Skaffa Azure Stack backup-konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ab404-112">Get Azure Stack backup configuration.</span></span>

## <span data-ttu-id="ab404-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ab404-113">PARAMETERS</span></span>

### <span data-ttu-id="ab404-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="ab404-114">-Location</span></span>
<span data-ttu-id="ab404-115">Plats för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="ab404-115">Backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab404-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab404-116">-ResourceGroupName</span></span>
<span data-ttu-id="ab404-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ab404-117">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab404-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab404-118">-ResourceId</span></span>
<span data-ttu-id="ab404-119">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="ab404-119">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab404-120">-Överst</span><span class="sxs-lookup"><span data-stu-id="ab404-120">-Top</span></span>
<span data-ttu-id="ab404-121">Returnera de översta N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ab404-121">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ab404-122">Gäller efter parametern-Skip.</span><span class="sxs-lookup"><span data-stu-id="ab404-122">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab404-123">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="ab404-123">-Skip</span></span>
<span data-ttu-id="ab404-124">Hoppa över de första N objekten enligt värdet i parametervärdet.</span><span class="sxs-lookup"><span data-stu-id="ab404-124">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab404-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab404-125">CommonParameters</span></span>
<span data-ttu-id="ab404-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab404-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab404-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab404-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab404-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ab404-128">INPUTS</span></span>

## <span data-ttu-id="ab404-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ab404-129">OUTPUTS</span></span>

### <span data-ttu-id="ab404-130">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="ab404-130">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="ab404-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ab404-131">NOTES</span></span>

## <span data-ttu-id="ab404-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ab404-132">RELATED LINKS</span></span>
