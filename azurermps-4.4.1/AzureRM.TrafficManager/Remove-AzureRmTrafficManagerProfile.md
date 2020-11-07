---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 5A4D685F-B904-4C85-8B68-C9936B0627FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 01a82084ddcea5fc3a5a3c412b7b6ea20dfcaa02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756311"
---
# <span data-ttu-id="1dc83-101">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-101">Remove-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="1dc83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dc83-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc83-103">Tar bort en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="1dc83-103">Deletes a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dc83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dc83-104">SYNTAX</span></span>

### <span data-ttu-id="1dc83-105">Fält</span><span class="sxs-lookup"><span data-stu-id="1dc83-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc83-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="1dc83-106">Object</span></span>
```
Remove-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc83-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dc83-107">DESCRIPTION</span></span>
<span data-ttu-id="1dc83-108">Cmdleten **Remove-AzureRmTrafficManagerProfile** tar bort en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="1dc83-108">The **Remove-AzureRmTrafficManagerProfile** cmdlet deletes an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1dc83-109">Ange profilen som ska tas bort med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="1dc83-109">Specify the profile to delete by using the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="1dc83-110">Alternativt kan du ange ett **TrafficManagerProfile** -objekt med parametern *TrafficManagerProfile* , eller så kan du använda pipeline.</span><span class="sxs-lookup"><span data-stu-id="1dc83-110">Alternatively, you can specify a **TrafficManagerProfile** object using the *TrafficManagerProfile* parameter, or you can use the pipeline.</span></span>

## <span data-ttu-id="1dc83-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dc83-111">EXAMPLES</span></span>

### <span data-ttu-id="1dc83-112">Exempel 1: ta bort en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="1dc83-112">Example 1: Delete a profile specified by name</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="1dc83-113">Det här kommandot tar bort profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1dc83-113">This command deletes the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="1dc83-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1dc83-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="1dc83-115">Exempel 2: ta bort en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="1dc83-115">Example 2: Delete a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Remove-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="1dc83-116">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1dc83-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="1dc83-117">Kommandot skickar sedan den profilen till cmdlet **Remove-AzureRmTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="1dc83-117">The command then passes that profile to the **Remove-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1dc83-118">Den profilen tas bort.</span><span class="sxs-lookup"><span data-stu-id="1dc83-118">That cmdlet deletes that profile.</span></span>
<span data-ttu-id="1dc83-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="1dc83-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="1dc83-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1dc83-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="1dc83-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dc83-121">PARAMETERS</span></span>

### <span data-ttu-id="1dc83-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc83-122">-Force</span></span>
<span data-ttu-id="1dc83-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="1dc83-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1dc83-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1dc83-124">-Name</span></span>
<span data-ttu-id="1dc83-125">Anger namnet på den Traffic Manager-profil som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="1dc83-125">Specifies the name of the Traffic Manager profile that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1dc83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc83-126">-ResourceGroupName</span></span>
<span data-ttu-id="1dc83-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="1dc83-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1dc83-128">Denna cmdlet tar bort en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="1dc83-128">This cmdlet deletes a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1dc83-129">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-129">-TrafficManagerProfile</span></span>
<span data-ttu-id="1dc83-130">Anger ett **TrafficManagerProfile** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="1dc83-130">Specifies a **TrafficManagerProfile** object to delete.</span></span>
<span data-ttu-id="1dc83-131">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="1dc83-131">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="1dc83-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1dc83-132">-Confirm</span></span>
<span data-ttu-id="1dc83-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dc83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc83-134">-WhatIf</span></span>
<span data-ttu-id="1dc83-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1dc83-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc83-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1dc83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc83-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-137">-DefaultProfile</span></span>
<span data-ttu-id="1dc83-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc83-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dc83-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc83-139">CommonParameters</span></span>
<span data-ttu-id="1dc83-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc83-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc83-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dc83-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc83-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dc83-142">INPUTS</span></span>

### <span data-ttu-id="1dc83-143">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="1dc83-144">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1dc83-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="1dc83-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dc83-145">OUTPUTS</span></span>

### <span data-ttu-id="1dc83-146">Returtyp</span><span class="sxs-lookup"><span data-stu-id="1dc83-146">Boolean</span></span>
<span data-ttu-id="1dc83-147">Denna cmdlet returnerar ett värde för $True, om det lyckas eller om det inte går att ta bort $False.</span><span class="sxs-lookup"><span data-stu-id="1dc83-147">This cmdlet returns a value of $True, if it succeeds or, if the deletion fails, a value of $False.</span></span>

## <span data-ttu-id="1dc83-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dc83-148">NOTES</span></span>

## <span data-ttu-id="1dc83-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dc83-149">RELATED LINKS</span></span>

[<span data-ttu-id="1dc83-150">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-150">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1dc83-151">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-151">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1dc83-152">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-152">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1dc83-153">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-153">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="1dc83-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1dc83-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)

