---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e714caedb86bd647ccc0692c47233833bc2db867
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573853"
---
# <span data-ttu-id="31a77-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="31a77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31a77-102">SYNOPSIS</span></span>
<span data-ttu-id="31a77-103">Inaktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="31a77-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31a77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31a77-104">SYNTAX</span></span>

### <span data-ttu-id="31a77-105">Fält</span><span class="sxs-lookup"><span data-stu-id="31a77-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31a77-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="31a77-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a77-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31a77-107">DESCRIPTION</span></span>
<span data-ttu-id="31a77-108">Cmdleten **disable-AzureRmTrafficManagerProfile** inaktiverar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="31a77-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="31a77-109">Du kan ange profil objekt med hjälp av pipeline eller som ett parameter värde.</span><span class="sxs-lookup"><span data-stu-id="31a77-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="31a77-110">Alternativt kan du ange profilen med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="31a77-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="31a77-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31a77-111">EXAMPLES</span></span>

### <span data-ttu-id="31a77-112">Exempel 1: inaktivera en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="31a77-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="31a77-113">Det här kommandot inaktiverar profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="31a77-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="31a77-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="31a77-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="31a77-115">Exempel 2: inaktivera en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="31a77-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="31a77-116">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="31a77-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="31a77-117">Då överförs den profilen till cmdleten **disable-AzureRmTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="31a77-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31a77-118">Denna cmdlet inaktiverar profilen.</span><span class="sxs-lookup"><span data-stu-id="31a77-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="31a77-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="31a77-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="31a77-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="31a77-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="31a77-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31a77-121">PARAMETERS</span></span>

### <span data-ttu-id="31a77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-122">-DefaultProfile</span></span>
<span data-ttu-id="31a77-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="31a77-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a77-124">-Force</span><span class="sxs-lookup"><span data-stu-id="31a77-124">-Force</span></span>
<span data-ttu-id="31a77-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="31a77-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31a77-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="31a77-126">-Name</span></span>
<span data-ttu-id="31a77-127">Anger namnet på den Traffic Manager-profil som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="31a77-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="31a77-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31a77-128">-ResourceGroupName</span></span>
<span data-ttu-id="31a77-129">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="31a77-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="31a77-130">Denna cmdlet inaktiverar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="31a77-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="31a77-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="31a77-132">Anger ett **TrafficManagerProfile** -objekt att inaktivera.</span><span class="sxs-lookup"><span data-stu-id="31a77-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="31a77-133">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="31a77-133">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="31a77-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="31a77-134">-Confirm</span></span>
<span data-ttu-id="31a77-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="31a77-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a77-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a77-136">-WhatIf</span></span>
<span data-ttu-id="31a77-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="31a77-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31a77-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="31a77-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a77-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a77-139">CommonParameters</span></span>
<span data-ttu-id="31a77-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a77-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a77-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a77-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a77-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31a77-142">INPUTS</span></span>

### <span data-ttu-id="31a77-143">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="31a77-144">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="31a77-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="31a77-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31a77-145">OUTPUTS</span></span>

### <span data-ttu-id="31a77-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31a77-146">System.Boolean</span></span>

## <span data-ttu-id="31a77-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31a77-147">NOTES</span></span>

## <span data-ttu-id="31a77-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31a77-148">RELATED LINKS</span></span>

[<span data-ttu-id="31a77-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="31a77-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="31a77-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="31a77-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="31a77-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="31a77-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


