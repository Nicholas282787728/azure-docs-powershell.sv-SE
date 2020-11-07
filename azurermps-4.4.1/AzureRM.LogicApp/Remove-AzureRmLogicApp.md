---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 6b76440b2d9e61075ac19e5a6fa0846a95a77669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756941"
---
# <span data-ttu-id="a4d93-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a4d93-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="a4d93-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4d93-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d93-103">Tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4d93-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4d93-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4d93-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d93-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4d93-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d93-106">Med cmdleten **Remove-AzureRmLogicApp** tar du bort ett logiskt program från en resurs grupp med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="a4d93-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="a4d93-107">Ange logik programmet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a4d93-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="a4d93-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="a4d93-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a4d93-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="a4d93-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a4d93-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="a4d93-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a4d93-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="a4d93-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a4d93-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4d93-112">EXAMPLES</span></span>

### <span data-ttu-id="a4d93-113">Exempel 1: ta bort ett logik program</span><span class="sxs-lookup"><span data-stu-id="a4d93-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="a4d93-114">Det här kommandot tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4d93-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="a4d93-115">Kommandot innehåller parametern *Force* , som hindrar kommandot från att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a4d93-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="a4d93-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4d93-116">PARAMETERS</span></span>

### <span data-ttu-id="a4d93-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a4d93-117">-Force</span></span>
<span data-ttu-id="a4d93-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a4d93-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a4d93-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a4d93-119">-Name</span></span>
<span data-ttu-id="a4d93-120">Anger namnet på det logik program som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a4d93-120">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a4d93-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d93-121">-ResourceGroupName</span></span>
<span data-ttu-id="a4d93-122">Anger namnet på den resurs grupp som innehåller det logik program som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="a4d93-122">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a4d93-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4d93-123">-Confirm</span></span>
<span data-ttu-id="a4d93-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4d93-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4d93-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d93-125">-WhatIf</span></span>
<span data-ttu-id="a4d93-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4d93-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4d93-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4d93-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4d93-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d93-128">-DefaultProfile</span></span>
<span data-ttu-id="a4d93-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4d93-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4d93-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d93-130">CommonParameters</span></span>
<span data-ttu-id="a4d93-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d93-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d93-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4d93-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d93-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4d93-133">INPUTS</span></span>

## <span data-ttu-id="a4d93-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4d93-134">OUTPUTS</span></span>

### <span data-ttu-id="a4d93-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="a4d93-135">System.Object</span></span>

## <span data-ttu-id="a4d93-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4d93-136">NOTES</span></span>

## <span data-ttu-id="a4d93-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4d93-137">RELATED LINKS</span></span>

[<span data-ttu-id="a4d93-138">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a4d93-138">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="a4d93-139">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a4d93-139">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="a4d93-140">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a4d93-140">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="a4d93-141">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a4d93-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


