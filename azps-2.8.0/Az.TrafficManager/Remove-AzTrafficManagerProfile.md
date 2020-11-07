---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerProfile.md
ms.openlocfilehash: 19f226d79e0de1b32aacae2beda22eae20d40afa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920817"
---
# <span data-ttu-id="0c541-101">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-101">Remove-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="0c541-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0c541-102">SYNOPSIS</span></span>
<span data-ttu-id="0c541-103">Tar bort en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="0c541-103">Deletes a Traffic Manager profile.</span></span>

## <span data-ttu-id="0c541-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0c541-104">SYNTAX</span></span>

### <span data-ttu-id="0c541-105">Fält</span><span class="sxs-lookup"><span data-stu-id="0c541-105">Fields</span></span>
```
Remove-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c541-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="0c541-106">Object</span></span>
```
Remove-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c541-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0c541-107">DESCRIPTION</span></span>
<span data-ttu-id="0c541-108">Cmdleten **Remove-AzTrafficManagerProfile** tar bort en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="0c541-108">The **Remove-AzTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0c541-109">Ange profilen som ska tas bort med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="0c541-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="0c541-110">Alternativt kan du ange ett **TrafficManagerProfile** -objekt med parametern *TrafficManagerProfile* , eller så kan du använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c541-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="0c541-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0c541-111">EXAMPLES</span></span>

### <span data-ttu-id="0c541-112">Exempel 1: ta bort en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="0c541-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="0c541-113">Det här kommandot tar bort profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0c541-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0c541-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0c541-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="0c541-115">Exempel 2: ta bort en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="0c541-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzTrafficManagerProfile -Force
```

<span data-ttu-id="0c541-116">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0c541-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="0c541-117">Kommandot skickar sedan den profilen till cmdlet **Remove-AzTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="0c541-117">The command then passes that profile to the **Remove-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0c541-118">Den profilen tas bort.</span><span class="sxs-lookup"><span data-stu-id="0c541-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="0c541-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="0c541-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0c541-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0c541-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0c541-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0c541-121">PARAMETERS</span></span>

### <span data-ttu-id="0c541-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-122">-DefaultProfile</span></span>
<span data-ttu-id="0c541-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0c541-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c541-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0c541-124">-Force</span></span>
<span data-ttu-id="0c541-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0c541-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c541-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="0c541-126">-Name</span></span>
<span data-ttu-id="0c541-127">Anger namnet på den Traffic Manager-profil som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="0c541-127">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c541-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c541-128">-ResourceGroupName</span></span>
<span data-ttu-id="0c541-129">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="0c541-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0c541-130">Denna cmdlet tar bort en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="0c541-130">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c541-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="0c541-132">Anger ett **TrafficManagerProfile** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="0c541-132">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="0c541-133">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="0c541-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c541-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0c541-134">-Confirm</span></span>
<span data-ttu-id="0c541-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0c541-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c541-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c541-136">-WhatIf</span></span>
<span data-ttu-id="0c541-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0c541-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c541-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0c541-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c541-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c541-139">CommonParameters</span></span>
<span data-ttu-id="0c541-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c541-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c541-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c541-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c541-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0c541-142">INPUTS</span></span>

### <span data-ttu-id="0c541-143">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="0c541-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0c541-144">OUTPUTS</span></span>

### <span data-ttu-id="0c541-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c541-145">System.Boolean</span></span>

## <span data-ttu-id="0c541-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0c541-146">NOTES</span></span>

## <span data-ttu-id="0c541-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0c541-147">RELATED LINKS</span></span>

[<span data-ttu-id="0c541-148">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-148">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="0c541-149">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-149">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="0c541-150">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-150">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="0c541-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="0c541-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c541-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


