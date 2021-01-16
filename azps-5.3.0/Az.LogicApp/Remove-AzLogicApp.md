---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523481"
---
# <span data-ttu-id="834d5-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="834d5-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="834d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="834d5-102">SYNOPSIS</span></span>
<span data-ttu-id="834d5-103">Tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="834d5-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="834d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="834d5-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="834d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="834d5-105">DESCRIPTION</span></span>
<span data-ttu-id="834d5-106">Med cmdleten **Remove-AzLogicApp** tar du bort ett logiskt program från en resurs grupp med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="834d5-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="834d5-107">Ange logik programmet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="834d5-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="834d5-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="834d5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="834d5-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="834d5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="834d5-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="834d5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="834d5-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="834d5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="834d5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="834d5-112">EXAMPLES</span></span>

### <span data-ttu-id="834d5-113">Exempel 1: ta bort ett logik program</span><span class="sxs-lookup"><span data-stu-id="834d5-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="834d5-114">Det här kommandot tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="834d5-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="834d5-115">Kommandot innehåller parametern *Force* , som hindrar kommandot från att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="834d5-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="834d5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="834d5-116">PARAMETERS</span></span>

### <span data-ttu-id="834d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="834d5-117">-DefaultProfile</span></span>
<span data-ttu-id="834d5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="834d5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="834d5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="834d5-119">-Force</span></span>
<span data-ttu-id="834d5-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="834d5-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="834d5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="834d5-121">-Name</span></span>
<span data-ttu-id="834d5-122">Anger namnet på det logik program som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="834d5-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="834d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="834d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="834d5-124">Anger namnet på den resurs grupp som innehåller det logik program som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="834d5-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="834d5-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="834d5-125">-Confirm</span></span>
<span data-ttu-id="834d5-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="834d5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="834d5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="834d5-127">-WhatIf</span></span>
<span data-ttu-id="834d5-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="834d5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="834d5-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="834d5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="834d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="834d5-130">CommonParameters</span></span>
<span data-ttu-id="834d5-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="834d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="834d5-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="834d5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="834d5-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="834d5-133">INPUTS</span></span>

### <span data-ttu-id="834d5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="834d5-134">System.String</span></span>

## <span data-ttu-id="834d5-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="834d5-135">OUTPUTS</span></span>

### <span data-ttu-id="834d5-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="834d5-136">System.Void</span></span>

## <span data-ttu-id="834d5-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="834d5-137">NOTES</span></span>

## <span data-ttu-id="834d5-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="834d5-138">RELATED LINKS</span></span>

[<span data-ttu-id="834d5-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="834d5-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="834d5-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="834d5-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="834d5-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="834d5-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="834d5-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="834d5-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


