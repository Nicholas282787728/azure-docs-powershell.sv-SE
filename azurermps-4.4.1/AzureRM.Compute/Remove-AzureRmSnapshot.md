---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 4c7260d3c1131ab573bf933f4b83022cef20819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585728"
---
# <span data-ttu-id="04120-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="04120-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="04120-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04120-102">SYNOPSIS</span></span>
<span data-ttu-id="04120-103">Tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="04120-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04120-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04120-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04120-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04120-105">DESCRIPTION</span></span>
<span data-ttu-id="04120-106">Cmdleten **Remove-AzureRmSnapshot** tar bort en stillbild.</span><span class="sxs-lookup"><span data-stu-id="04120-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="04120-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04120-107">EXAMPLES</span></span>

### <span data-ttu-id="04120-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04120-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="04120-109">Det här kommandot tar bort stillbilden "Snapshot01" i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="04120-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="04120-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04120-110">PARAMETERS</span></span>

### <span data-ttu-id="04120-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04120-111">-DefaultProfile</span></span>
<span data-ttu-id="04120-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04120-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04120-113">-Force</span><span class="sxs-lookup"><span data-stu-id="04120-113">-Force</span></span>
<span data-ttu-id="04120-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="04120-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04120-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04120-115">-ResourceGroupName</span></span>
<span data-ttu-id="04120-116">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="04120-116">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04120-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="04120-117">-SnapshotName</span></span>
<span data-ttu-id="04120-118">Anger namnet på en ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="04120-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04120-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04120-119">-Confirm</span></span>
<span data-ttu-id="04120-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04120-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04120-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04120-121">-WhatIf</span></span>
<span data-ttu-id="04120-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04120-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04120-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04120-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04120-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04120-124">CommonParameters</span></span>
<span data-ttu-id="04120-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04120-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04120-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04120-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04120-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04120-127">INPUTS</span></span>

### <span data-ttu-id="04120-128">System. String</span><span class="sxs-lookup"><span data-stu-id="04120-128">System.String</span></span>

## <span data-ttu-id="04120-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04120-129">OUTPUTS</span></span>

### <span data-ttu-id="04120-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="04120-130">System.Object</span></span>

## <span data-ttu-id="04120-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04120-131">NOTES</span></span>

## <span data-ttu-id="04120-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04120-132">RELATED LINKS</span></span>

