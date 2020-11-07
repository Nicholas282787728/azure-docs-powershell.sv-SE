---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744343"
---
# <span data-ttu-id="6a879-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="6a879-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="6a879-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6a879-102">SYNOPSIS</span></span>
<span data-ttu-id="6a879-103">Hämtar policyn för automatisk avslutning av ett labb i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="6a879-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="6a879-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6a879-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a879-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6a879-105">DESCRIPTION</span></span>
<span data-ttu-id="6a879-106">Cmdleten **Get-AzDtlAutoShutdownPolicy** hämtar den automatiska avslutnings principen för ett labb, vilket gör att du automatiskt kan stänga av alla virtuella datorer i ett labb under en viss tid.</span><span class="sxs-lookup"><span data-stu-id="6a879-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="6a879-107">Cmdleten returnerar om principens status är aktive rad och den tid som du har angett för att stänga av virtuella laboratorie datorer automatiskt.</span><span class="sxs-lookup"><span data-stu-id="6a879-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="6a879-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6a879-108">EXAMPLES</span></span>

## <span data-ttu-id="6a879-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6a879-109">PARAMETERS</span></span>

### <span data-ttu-id="6a879-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a879-110">-DefaultProfile</span></span>
<span data-ttu-id="6a879-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6a879-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a879-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="6a879-112">-LabName</span></span>
<span data-ttu-id="6a879-113">Anger namnet på den Lab för vilken denna cmdlet får principen för automatisk avstängning.</span><span class="sxs-lookup"><span data-stu-id="6a879-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a879-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a879-114">-ResourceGroupName</span></span>
<span data-ttu-id="6a879-115">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="6a879-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="6a879-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a879-116">CommonParameters</span></span>
<span data-ttu-id="6a879-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a879-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a879-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a879-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a879-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6a879-119">INPUTS</span></span>

### <span data-ttu-id="6a879-120">System. String</span><span class="sxs-lookup"><span data-stu-id="6a879-120">System.String</span></span>

## <span data-ttu-id="6a879-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6a879-121">OUTPUTS</span></span>

### <span data-ttu-id="6a879-122">Microsoft. Azure. commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="6a879-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="6a879-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6a879-123">NOTES</span></span>

## <span data-ttu-id="6a879-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6a879-124">RELATED LINKS</span></span>

[<span data-ttu-id="6a879-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="6a879-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)

