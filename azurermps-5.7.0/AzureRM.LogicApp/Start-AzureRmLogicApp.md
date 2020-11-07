---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: fefe9da2d0339c22d0f41e1526d8664ff27a52d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758223"
---
# <span data-ttu-id="99d14-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99d14-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="99d14-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99d14-102">SYNOPSIS</span></span>
<span data-ttu-id="99d14-103">Kör ett logiskt program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="99d14-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99d14-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99d14-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99d14-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99d14-105">DESCRIPTION</span></span>
<span data-ttu-id="99d14-106">Cmdleten **Start-AzureRmLogicApp** kör ett logiskt program med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="99d14-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="99d14-107">Ange ett namn, en resurs grupp och en utlösare.</span><span class="sxs-lookup"><span data-stu-id="99d14-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="99d14-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="99d14-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="99d14-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="99d14-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="99d14-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="99d14-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="99d14-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="99d14-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="99d14-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99d14-112">EXAMPLES</span></span>

### <span data-ttu-id="99d14-113">Exempel 1: kör ett logiskt program</span><span class="sxs-lookup"><span data-stu-id="99d14-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="99d14-114">Det här kommandot kör programmet logik i resurs gruppen som heter ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="99d14-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="99d14-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99d14-115">PARAMETERS</span></span>

### <span data-ttu-id="99d14-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99d14-116">-DefaultProfile</span></span>
<span data-ttu-id="99d14-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99d14-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99d14-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="99d14-118">-Name</span></span>
<span data-ttu-id="99d14-119">Anger namnet på det logik program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="99d14-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="99d14-120">-Parametrar</span><span class="sxs-lookup"><span data-stu-id="99d14-120">-Parameters</span></span>
<span data-ttu-id="99d14-121">Anger ett samlings objekt i logik programmet.</span><span class="sxs-lookup"><span data-stu-id="99d14-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="99d14-122">Ange en hash-tabell, en ord lista \<string\> eller en ord lista \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="99d14-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d14-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99d14-123">-ResourceGroupName</span></span>
<span data-ttu-id="99d14-124">Anger namnet på den resurs grupp som innehåller det logik program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="99d14-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="99d14-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="99d14-125">-TriggerName</span></span>
<span data-ttu-id="99d14-126">Anger namnet på den lösnings program som den här cmdleten startar.</span><span class="sxs-lookup"><span data-stu-id="99d14-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="99d14-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99d14-127">-Confirm</span></span>
<span data-ttu-id="99d14-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99d14-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99d14-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99d14-129">-WhatIf</span></span>
<span data-ttu-id="99d14-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99d14-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99d14-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99d14-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99d14-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d14-132">CommonParameters</span></span>
<span data-ttu-id="99d14-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d14-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d14-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d14-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d14-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99d14-135">INPUTS</span></span>

### <span data-ttu-id="99d14-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="99d14-136">None</span></span>
<span data-ttu-id="99d14-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="99d14-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99d14-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99d14-138">OUTPUTS</span></span>

### <span data-ttu-id="99d14-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="99d14-139">System.Object</span></span>

## <span data-ttu-id="99d14-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99d14-140">NOTES</span></span>

## <span data-ttu-id="99d14-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99d14-141">RELATED LINKS</span></span>

[<span data-ttu-id="99d14-142">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99d14-142">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="99d14-143">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="99d14-143">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="99d14-144">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99d14-144">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="99d14-145">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99d14-145">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="99d14-146">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="99d14-146">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="99d14-147">Stopp-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="99d14-147">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


