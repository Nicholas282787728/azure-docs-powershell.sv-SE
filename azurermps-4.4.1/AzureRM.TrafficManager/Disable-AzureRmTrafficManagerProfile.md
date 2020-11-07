---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: c3a32c6bab916ad4a63db5e528e00fe3948a1d2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755786"
---
# <span data-ttu-id="a0fb0-101">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-101">Disable-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="a0fb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="a0fb0-103">Inaktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-103">Disables a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0fb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0fb0-104">SYNTAX</span></span>

### <span data-ttu-id="a0fb0-105">Fält</span><span class="sxs-lookup"><span data-stu-id="a0fb0-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0fb0-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="a0fb0-106">Object</span></span>
```
Disable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0fb0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0fb0-107">DESCRIPTION</span></span>
<span data-ttu-id="a0fb0-108">Cmdleten **disable-AzureRmTrafficManagerProfile** inaktiverar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-108">The **Disable-AzureRmTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="a0fb0-109">Du kan ange profil objekt med hjälp av pipeline eller som ett parameter värde.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="a0fb0-110">Alternativt kan du ange profilen med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="a0fb0-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="a0fb0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0fb0-111">EXAMPLES</span></span>

### <span data-ttu-id="a0fb0-112">Exempel 1: inaktivera en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="a0fb0-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a0fb0-113">Det här kommandot inaktiverar profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a0fb0-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="a0fb0-115">Exempel 2: inaktivera en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="a0fb0-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerProfile -Force
```

<span data-ttu-id="a0fb0-116">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="a0fb0-117">Då överförs den profilen till cmdleten **disable-AzureRmTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-117">The command then passes that profile to the **Disable-AzureRmTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a0fb0-118">Denna cmdlet inaktiverar profilen.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="a0fb0-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="a0fb0-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a0fb0-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a0fb0-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0fb0-121">PARAMETERS</span></span>

### <span data-ttu-id="a0fb0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a0fb0-122">-Force</span></span>
<span data-ttu-id="a0fb0-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0fb0-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0fb0-124">-Name</span></span>
<span data-ttu-id="a0fb0-125">Anger namnet på den Traffic Manager-profil som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-125">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="a0fb0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0fb0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0fb0-127">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a0fb0-128">Denna cmdlet inaktiverar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-128">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0fb0-129">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-129">-TrafficManagerProfile</span></span>
<span data-ttu-id="a0fb0-130">Anger ett **TrafficManagerProfile** -objekt att inaktivera.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-130">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="a0fb0-131">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-131">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="a0fb0-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0fb0-132">-Confirm</span></span>
<span data-ttu-id="a0fb0-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0fb0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0fb0-134">-WhatIf</span></span>
<span data-ttu-id="a0fb0-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0fb0-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0fb0-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-137">-DefaultProfile</span></span>
<span data-ttu-id="a0fb0-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0fb0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0fb0-139">CommonParameters</span></span>
<span data-ttu-id="a0fb0-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0fb0-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0fb0-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0fb0-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0fb0-142">INPUTS</span></span>

### <span data-ttu-id="a0fb0-143">Microsoft. Azure. commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-143">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="a0fb0-144">Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a0fb0-144">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="a0fb0-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0fb0-145">OUTPUTS</span></span>

### <span data-ttu-id="a0fb0-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0fb0-146">System.Boolean</span></span>

## <span data-ttu-id="a0fb0-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0fb0-147">NOTES</span></span>

## <span data-ttu-id="a0fb0-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0fb0-148">RELATED LINKS</span></span>

[<span data-ttu-id="a0fb0-149">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-149">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0fb0-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0fb0-151">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-151">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0fb0-152">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-152">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="a0fb0-153">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a0fb0-153">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


