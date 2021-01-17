---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415544"
---
# <span data-ttu-id="c1aab-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c1aab-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="c1aab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1aab-102">SYNOPSIS</span></span>
<span data-ttu-id="c1aab-103">Kör ett logiskt program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c1aab-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="c1aab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1aab-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1aab-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1aab-105">DESCRIPTION</span></span>
<span data-ttu-id="c1aab-106">Cmdleten **Start-AzLogicApp** kör ett logiskt program med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="c1aab-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="c1aab-107">Ange ett namn, en resurs grupp och en utlösare.</span><span class="sxs-lookup"><span data-stu-id="c1aab-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="c1aab-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="c1aab-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c1aab-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="c1aab-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c1aab-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="c1aab-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c1aab-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="c1aab-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c1aab-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1aab-112">EXAMPLES</span></span>

### <span data-ttu-id="c1aab-113">Exempel 1: kör ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="c1aab-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="c1aab-114">Det här kommandot kör programmet logik i resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="c1aab-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="c1aab-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1aab-115">PARAMETERS</span></span>

### <span data-ttu-id="c1aab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1aab-116">-DefaultProfile</span></span>
<span data-ttu-id="c1aab-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c1aab-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1aab-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1aab-118">-Name</span></span>
<span data-ttu-id="c1aab-119">Anger namnet på det logik program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="c1aab-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="c1aab-120">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="c1aab-120">-Parameters</span></span>
<span data-ttu-id="c1aab-121">Anger ett samlings objekt i logik programmet.</span><span class="sxs-lookup"><span data-stu-id="c1aab-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="c1aab-122">Ange en hash-tabell, en ord lista \<string\> eller en ord lista \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="c1aab-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1aab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1aab-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1aab-124">Anger namnet på den resurs grupp som innehåller det logik program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="c1aab-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="c1aab-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="c1aab-125">-TriggerName</span></span>
<span data-ttu-id="c1aab-126">Anger namnet på den lösnings program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="c1aab-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="c1aab-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1aab-127">-Confirm</span></span>
<span data-ttu-id="c1aab-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1aab-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1aab-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1aab-129">-WhatIf</span></span>
<span data-ttu-id="c1aab-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1aab-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1aab-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1aab-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1aab-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1aab-132">CommonParameters</span></span>
<span data-ttu-id="c1aab-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1aab-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1aab-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1aab-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1aab-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1aab-135">INPUTS</span></span>

### <span data-ttu-id="c1aab-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c1aab-136">System.String</span></span>

## <span data-ttu-id="c1aab-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1aab-137">OUTPUTS</span></span>

### <span data-ttu-id="c1aab-138">System. Void</span><span class="sxs-lookup"><span data-stu-id="c1aab-138">System.Void</span></span>

## <span data-ttu-id="c1aab-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1aab-139">NOTES</span></span>

## <span data-ttu-id="c1aab-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1aab-140">RELATED LINKS</span></span>

[<span data-ttu-id="c1aab-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c1aab-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="c1aab-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c1aab-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="c1aab-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c1aab-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="c1aab-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c1aab-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="c1aab-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="c1aab-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="c1aab-146">Stopp-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="c1aab-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


