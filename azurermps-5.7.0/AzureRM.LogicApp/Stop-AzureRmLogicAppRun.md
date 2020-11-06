---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 3308F901-4C9F-424D-8BEB-877A6038B246
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/stop-azurermlogicapprun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Stop-AzureRmLogicAppRun.md
ms.openlocfilehash: 1d23c4f92a73a2ec6471169a05c1048d96abcaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577191"
---
# <span data-ttu-id="2534f-101">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="2534f-101">Stop-AzureRmLogicAppRun</span></span>

## <span data-ttu-id="2534f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2534f-102">SYNOPSIS</span></span>
<span data-ttu-id="2534f-103">Avbryter en körning av ett logik program.</span><span class="sxs-lookup"><span data-stu-id="2534f-103">Cancels a run of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2534f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2534f-104">SYNTAX</span></span>

```
Stop-AzureRmLogicAppRun -ResourceGroupName <String> -Name <String> -RunName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2534f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2534f-105">DESCRIPTION</span></span>
<span data-ttu-id="2534f-106">Cmdleten **Stop-AzureRmLogicAppRun** avbryter en körning av ett logik program.</span><span class="sxs-lookup"><span data-stu-id="2534f-106">The **Stop-AzureRmLogicAppRun** cmdlet cancels a run of a logic app.</span></span>
<span data-ttu-id="2534f-107">Ange logik program, resurs grupp och kör.</span><span class="sxs-lookup"><span data-stu-id="2534f-107">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="2534f-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="2534f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2534f-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="2534f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2534f-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="2534f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2534f-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="2534f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2534f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2534f-112">EXAMPLES</span></span>

### <span data-ttu-id="2534f-113">Exempel 1: avbryta en körning av ett logik program</span><span class="sxs-lookup"><span data-stu-id="2534f-113">Example 1: Cancel a run of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -RunName "08587489104702792076"
```

<span data-ttu-id="2534f-114">Det här kommandot avbryter en körning av logik programmet som heter LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="2534f-114">This command cancels a run of the logic app named LogicApp03.</span></span>

## <span data-ttu-id="2534f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2534f-115">PARAMETERS</span></span>

### <span data-ttu-id="2534f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2534f-116">-DefaultProfile</span></span>
<span data-ttu-id="2534f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2534f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2534f-118">-Force</span></span>
<span data-ttu-id="2534f-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2534f-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2534f-120">-Name</span></span>
<span data-ttu-id="2534f-121">Anger namnet på en logik-app för vilken denna cmdlet avbryter en körning.</span><span class="sxs-lookup"><span data-stu-id="2534f-121">Specifies the name of a logic app for which this cmdlet cancels a run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2534f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2534f-123">Anger namnet på en resurs grupp där denna cmdlet avbryter en körning.</span><span class="sxs-lookup"><span data-stu-id="2534f-123">Specifies the name for a resource group in which this cmdlet cancels a run.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-124">-RunName</span><span class="sxs-lookup"><span data-stu-id="2534f-124">-RunName</span></span>
<span data-ttu-id="2534f-125">Anger namnet på en logik-app som ska köras om denna cmdlet avbryts.</span><span class="sxs-lookup"><span data-stu-id="2534f-125">Specifies the name of a logic app run that this cmdlet cancels.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2534f-126">-Confirm</span></span>
<span data-ttu-id="2534f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2534f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2534f-128">-WhatIf</span></span>
<span data-ttu-id="2534f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2534f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2534f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2534f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2534f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2534f-131">CommonParameters</span></span>
<span data-ttu-id="2534f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2534f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2534f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2534f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2534f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2534f-134">INPUTS</span></span>

### <span data-ttu-id="2534f-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="2534f-135">None</span></span>
<span data-ttu-id="2534f-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="2534f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2534f-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2534f-137">OUTPUTS</span></span>

### <span data-ttu-id="2534f-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="2534f-138">System.Object</span></span>

## <span data-ttu-id="2534f-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2534f-139">NOTES</span></span>

## <span data-ttu-id="2534f-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2534f-140">RELATED LINKS</span></span>

[<span data-ttu-id="2534f-141">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2534f-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


