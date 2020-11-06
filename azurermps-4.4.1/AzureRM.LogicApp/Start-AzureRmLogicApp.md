---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: ed8a8c198f626d569d47a9b06b6d9595517f2f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586491"
---
# <span data-ttu-id="8c53f-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c53f-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="8c53f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c53f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c53f-103">Kör ett logiskt program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="8c53f-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c53f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c53f-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c53f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c53f-105">DESCRIPTION</span></span>
<span data-ttu-id="8c53f-106">Cmdleten **Start-AzureRmLogicApp** kör ett logiskt program med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="8c53f-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="8c53f-107">Ange ett namn, en resurs grupp och en utlösare.</span><span class="sxs-lookup"><span data-stu-id="8c53f-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="8c53f-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="8c53f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8c53f-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="8c53f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8c53f-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="8c53f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8c53f-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="8c53f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8c53f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c53f-112">EXAMPLES</span></span>

### <span data-ttu-id="8c53f-113">Exempel 1: kör ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="8c53f-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="8c53f-114">Det här kommandot kör programmet logik i resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8c53f-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8c53f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c53f-115">PARAMETERS</span></span>

### <span data-ttu-id="8c53f-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c53f-116">-Name</span></span>
<span data-ttu-id="8c53f-117">Anger namnet på det logik program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="8c53f-117">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8c53f-118">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="8c53f-118">-Parameters</span></span>
<span data-ttu-id="8c53f-119">Anger ett samlings objekt i logik programmet.</span><span class="sxs-lookup"><span data-stu-id="8c53f-119">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="8c53f-120">Ange en hash-tabell, en ord lista \<string\> eller en ord lista \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="8c53f-120">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="8c53f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c53f-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c53f-122">Anger namnet på den resurs grupp som innehåller det logik program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="8c53f-122">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8c53f-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="8c53f-123">-TriggerName</span></span>
<span data-ttu-id="8c53f-124">Anger namnet på den lösnings program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="8c53f-124">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8c53f-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c53f-125">-Confirm</span></span>
<span data-ttu-id="8c53f-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c53f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c53f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c53f-127">-WhatIf</span></span>
<span data-ttu-id="8c53f-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c53f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c53f-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c53f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c53f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c53f-130">-DefaultProfile</span></span>
<span data-ttu-id="8c53f-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c53f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c53f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c53f-132">CommonParameters</span></span>
<span data-ttu-id="8c53f-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c53f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c53f-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c53f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c53f-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c53f-135">INPUTS</span></span>

## <span data-ttu-id="8c53f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c53f-136">OUTPUTS</span></span>

### <span data-ttu-id="8c53f-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="8c53f-137">System.Object</span></span>

## <span data-ttu-id="8c53f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c53f-138">NOTES</span></span>

## <span data-ttu-id="8c53f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c53f-139">RELATED LINKS</span></span>

[<span data-ttu-id="8c53f-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c53f-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="8c53f-141">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="8c53f-141">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="8c53f-142">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c53f-142">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="8c53f-143">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c53f-143">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="8c53f-144">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8c53f-144">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="8c53f-145">Stopp-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="8c53f-145">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


