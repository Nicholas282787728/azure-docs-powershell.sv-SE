---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/stop-azlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Stop-AzLogicAppRun.md
ms.openlocfilehash: 9a437d3b8e1803865aedf7e46d0bf879cfcdeab8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088139"
---
# <span data-ttu-id="bc519-101">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="bc519-101">Stop-AzLogicAppRun</span></span>

## <span data-ttu-id="bc519-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc519-102">SYNOPSIS</span></span>
<span data-ttu-id="bc519-103">Avbryter en körning av ett logik program.</span><span class="sxs-lookup"><span data-stu-id="bc519-103">Cancels a run of a logic app.</span></span>

## <span data-ttu-id="bc519-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc519-104">SYNTAX</span></span>

```
Stop-AzLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc519-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc519-105">DESCRIPTION</span></span>
<span data-ttu-id="bc519-106">Cmdleten **Stop-AzLogicAppRun** avbryter en körning av ett logik program.</span><span class="sxs-lookup"><span data-stu-id="bc519-106">The **Stop-AzLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="bc519-107">Ange logik program, resurs grupp och kör.</span><span class="sxs-lookup"><span data-stu-id="bc519-107">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="bc519-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="bc519-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bc519-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="bc519-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bc519-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="bc519-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bc519-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="bc519-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bc519-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc519-112">EXAMPLES</span></span>

### <span data-ttu-id="bc519-113">Exempel 1: avbryta en körning av ett logik program</span><span class="sxs-lookup"><span data-stu-id="bc519-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Stop-AzLogicAppRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076" -Force
```

<span data-ttu-id="bc519-114">Det här kommandot avbryter en körning av logik programmet som heter LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="bc519-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="bc519-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc519-115">PARAMETERS</span></span>

### <span data-ttu-id="bc519-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc519-116">-DefaultProfile</span></span>
<span data-ttu-id="bc519-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bc519-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc519-118">-Force</span><span class="sxs-lookup"><span data-stu-id="bc519-118">-Force</span></span>
<span data-ttu-id="bc519-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bc519-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bc519-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="bc519-120">-Name</span></span>
<span data-ttu-id="bc519-121">Anger namnet på en logik-app för vilken denna cmdlet avbryter en körning.</span><span class="sxs-lookup"><span data-stu-id="bc519-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc519-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc519-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc519-123">Anger namnet på en resurs grupp där denna cmdlet avbryter en körning.</span><span class="sxs-lookup"><span data-stu-id="bc519-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc519-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="bc519-124">-RunName</span></span>
<span data-ttu-id="bc519-125">Anger namnet på en logik-app som ska köras om denna cmdlet avbryts.</span><span class="sxs-lookup"><span data-stu-id="bc519-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc519-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc519-126">-Confirm</span></span>
<span data-ttu-id="bc519-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc519-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc519-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc519-128">-WhatIf</span></span>
<span data-ttu-id="bc519-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc519-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc519-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc519-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc519-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc519-131">CommonParameters</span></span>
<span data-ttu-id="bc519-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc519-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc519-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc519-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc519-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc519-134">INPUTS</span></span>

### <span data-ttu-id="bc519-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bc519-135">System.String</span></span>

## <span data-ttu-id="bc519-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc519-136">OUTPUTS</span></span>

### <span data-ttu-id="bc519-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="bc519-137">System.Void</span></span>

## <span data-ttu-id="bc519-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc519-138">NOTES</span></span>

## <span data-ttu-id="bc519-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc519-139">RELATED LINKS</span></span>

[<span data-ttu-id="bc519-140">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="bc519-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


