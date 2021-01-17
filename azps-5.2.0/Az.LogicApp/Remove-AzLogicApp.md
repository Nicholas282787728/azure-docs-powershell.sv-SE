---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405211"
---
# <span data-ttu-id="696be-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="696be-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="696be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="696be-102">SYNOPSIS</span></span>
<span data-ttu-id="696be-103">Tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="696be-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="696be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="696be-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="696be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="696be-105">DESCRIPTION</span></span>
<span data-ttu-id="696be-106">Med cmdleten **Remove-AzLogicApp** tar du bort ett logiskt program från en resurs grupp med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="696be-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="696be-107">Ange logik programmet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="696be-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="696be-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="696be-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="696be-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="696be-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="696be-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="696be-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="696be-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="696be-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="696be-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="696be-112">EXAMPLES</span></span>

### <span data-ttu-id="696be-113">Exempel 1: ta bort ett logik program</span><span class="sxs-lookup"><span data-stu-id="696be-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="696be-114">Det här kommandot tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="696be-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="696be-115">Kommandot innehåller parametern *Force* , som hindrar kommandot från att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="696be-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="696be-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="696be-116">PARAMETERS</span></span>

### <span data-ttu-id="696be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696be-117">-DefaultProfile</span></span>
<span data-ttu-id="696be-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="696be-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="696be-119">-Force</span><span class="sxs-lookup"><span data-stu-id="696be-119">-Force</span></span>
<span data-ttu-id="696be-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="696be-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="696be-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="696be-121">-Name</span></span>
<span data-ttu-id="696be-122">Anger namnet på det logik program som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="696be-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="696be-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696be-123">-ResourceGroupName</span></span>
<span data-ttu-id="696be-124">Anger namnet på den resurs grupp som innehåller det logik program som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="696be-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="696be-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="696be-125">-Confirm</span></span>
<span data-ttu-id="696be-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="696be-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696be-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696be-127">-WhatIf</span></span>
<span data-ttu-id="696be-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="696be-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696be-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="696be-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696be-130">CommonParameters</span></span>
<span data-ttu-id="696be-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696be-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696be-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696be-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="696be-133">INPUTS</span></span>

### <span data-ttu-id="696be-134">System. String</span><span class="sxs-lookup"><span data-stu-id="696be-134">System.String</span></span>

## <span data-ttu-id="696be-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="696be-135">OUTPUTS</span></span>

### <span data-ttu-id="696be-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="696be-136">System.Void</span></span>

## <span data-ttu-id="696be-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="696be-137">NOTES</span></span>

## <span data-ttu-id="696be-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="696be-138">RELATED LINKS</span></span>

[<span data-ttu-id="696be-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="696be-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="696be-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="696be-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="696be-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="696be-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="696be-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="696be-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


