---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: B6E043FF-F4DD-44B7-BEAA-6B17C8F21D58
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerProfile.md
ms.openlocfilehash: fc1370da73b9217c5f5f8b24705047f154b50f31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272504"
---
# <span data-ttu-id="9abae-101">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-101">Disable-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="9abae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9abae-102">SYNOPSIS</span></span>
<span data-ttu-id="9abae-103">Inaktiverar en Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="9abae-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="9abae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9abae-104">SYNTAX</span></span>

### <span data-ttu-id="9abae-105">Fält</span><span class="sxs-lookup"><span data-stu-id="9abae-105">Fields</span></span>
```
Disable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9abae-106">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="9abae-106">Object</span></span>
```
Disable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9abae-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9abae-107">DESCRIPTION</span></span>
<span data-ttu-id="9abae-108">Cmdleten **disable-AzTrafficManagerProfile** inaktiverar en Azure Traffic Manager-profil.</span><span class="sxs-lookup"><span data-stu-id="9abae-108">The **Disable-AzTrafficManagerProfile** cmdlet disables an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9abae-109">Du kan ange profil objekt med hjälp av pipeline eller som ett parameter värde.</span><span class="sxs-lookup"><span data-stu-id="9abae-109">You can specify the profile object by using the pipeline or as a parameter value.</span></span>
<span data-ttu-id="9abae-110">Alternativt kan du ange profilen med hjälp av parametrarna *Name* och *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="9abae-110">Alternatively, you can specify the profile by using the *Name* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="9abae-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9abae-111">EXAMPLES</span></span>

### <span data-ttu-id="9abae-112">Exempel 1: inaktivera en profil som anges med namn</span><span class="sxs-lookup"><span data-stu-id="9abae-112">Example 1: Disable a profile specified by name</span></span>
```
PS C:\>Disable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9abae-113">Det här kommandot inaktiverar profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9abae-113">This command disables the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9abae-114">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9abae-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="9abae-115">Exempel 2: inaktivera en profil med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="9abae-115">Example 2: Disable a profile by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerProfile -Force
```

<span data-ttu-id="9abae-116">Det här kommandot får profilen med namnet ContosoProfile i ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9abae-116">This command gets the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="9abae-117">Då överförs den profilen till cmdleten **disable-AzTrafficManagerProfile** med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="9abae-117">The command then passes that profile to the **Disable-AzTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9abae-118">Denna cmdlet inaktiverar profilen.</span><span class="sxs-lookup"><span data-stu-id="9abae-118">That cmdlet disables that profile.</span></span>
<span data-ttu-id="9abae-119">Kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="9abae-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="9abae-120">Därför behöver du inte bekräfta.</span><span class="sxs-lookup"><span data-stu-id="9abae-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="9abae-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9abae-121">PARAMETERS</span></span>

### <span data-ttu-id="9abae-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-122">-DefaultProfile</span></span>
<span data-ttu-id="9abae-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9abae-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9abae-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9abae-124">-Force</span></span>
<span data-ttu-id="9abae-125">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9abae-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9abae-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="9abae-126">-Name</span></span>
<span data-ttu-id="9abae-127">Anger namnet på den Traffic Manager-profil som denna cmdlet inaktiverar.</span><span class="sxs-lookup"><span data-stu-id="9abae-127">Specifies the name of the Traffic Manager profile that this cmdlet disables.</span></span>

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

### <span data-ttu-id="9abae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9abae-128">-ResourceGroupName</span></span>
<span data-ttu-id="9abae-129">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9abae-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9abae-130">Denna cmdlet inaktiverar en Traffic Manager-profil i gruppen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="9abae-130">This cmdlet disables a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9abae-131">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-131">-TrafficManagerProfile</span></span>
<span data-ttu-id="9abae-132">Anger ett **TrafficManagerProfile** -objekt att inaktivera.</span><span class="sxs-lookup"><span data-stu-id="9abae-132">Specifies a **TrafficManagerProfile** object to disable.</span></span>
<span data-ttu-id="9abae-133">För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9abae-133">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="9abae-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9abae-134">-Confirm</span></span>
<span data-ttu-id="9abae-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9abae-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abae-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abae-136">-WhatIf</span></span>
<span data-ttu-id="9abae-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9abae-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abae-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9abae-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abae-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abae-139">CommonParameters</span></span>
<span data-ttu-id="9abae-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abae-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abae-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9abae-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abae-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9abae-142">INPUTS</span></span>

### <span data-ttu-id="9abae-143">Microsoft. Azure. commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9abae-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9abae-144">OUTPUTS</span></span>

### <span data-ttu-id="9abae-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9abae-145">System.Boolean</span></span>

## <span data-ttu-id="9abae-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9abae-146">NOTES</span></span>

## <span data-ttu-id="9abae-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9abae-147">RELATED LINKS</span></span>

[<span data-ttu-id="9abae-148">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-148">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="9abae-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9abae-150">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-150">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="9abae-151">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-151">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="9abae-152">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9abae-152">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


