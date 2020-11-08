---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100641"
---
# <span data-ttu-id="84c4c-101">Remove-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="84c4c-101">Remove-WAPackVMRole</span></span>

## <span data-ttu-id="84c4c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84c4c-102">SYNOPSIS</span></span>
<span data-ttu-id="84c4c-103">Tar bort roll objekt för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="84c4c-103">Removes virtual machine role objects.</span></span>

## <span data-ttu-id="84c4c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84c4c-104">SYNTAX</span></span>

### <span data-ttu-id="84c4c-105">FromVMRoleObject (standard)</span><span class="sxs-lookup"><span data-stu-id="84c4c-105">FromVMRoleObject (Default)</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84c4c-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="84c4c-106">FromCloudService</span></span>
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84c4c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84c4c-107">DESCRIPTION</span></span>
<span data-ttu-id="84c4c-108">De här ämnena är föråldrade och kommer att tas bort i framtiden.</span><span class="sxs-lookup"><span data-stu-id="84c4c-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="84c4c-109">I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="84c4c-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="84c4c-110">För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="84c4c-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="84c4c-111">Cmdleten **Remove-WAPackVMRole** tar bort roll objekt för virtuella datorer.</span><span class="sxs-lookup"><span data-stu-id="84c4c-111">The **Remove-WAPackVMRole** cmdlet removes virtual machine role objects.</span></span>

## <span data-ttu-id="84c4c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84c4c-112">EXAMPLES</span></span>

### <span data-ttu-id="84c4c-113">Exempel 1: ta bort en virtuell dator roll (som skapades med WAP-portalen)</span><span class="sxs-lookup"><span data-stu-id="84c4c-113">Example 1: Remove a virtual machine role (which was created using the WAP portal)</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

<span data-ttu-id="84c4c-114">Det första kommandot får rollen virtuell dator med namnet ContosoVMRole01 med hjälp av cmdleten **Get-WAPackVMRole** och lagrar sedan objektet i variabeln $VMRole.</span><span class="sxs-lookup"><span data-stu-id="84c4c-114">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="84c4c-115">Det andra kommandot tar bort den virtuella dator rollen som lagras i $VMRole.</span><span class="sxs-lookup"><span data-stu-id="84c4c-115">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="84c4c-116">Med kommandot uppmanas du att bekräfta. Förutsatt att den här virtuella dator rollen skapades med WAP-portalen behöver du inte ange namnet på moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="84c4c-116">The command prompts you for confirmation.Assuming this virtual machine role was created using the WAP portal, there's no need to specify the cloud service name.</span></span>

### <span data-ttu-id="84c4c-117">Exempel 2: ta bort en virtuell dator roll som skapades när du skapade en moln tjänst manuellt</span><span class="sxs-lookup"><span data-stu-id="84c4c-117">Example 2: Remove a virtual machine role which was created after manually creating a cloud service</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

<span data-ttu-id="84c4c-118">Det första kommandot får rollen virtuell dator med namnet "ContosoVMRole02" med cmdleten **Get-WAPackVMRole** och lagrar sedan objektet i variabeln $VMRole.</span><span class="sxs-lookup"><span data-stu-id="84c4c-118">The first command gets the virtual machine role named "ContosoVMRole02" by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="84c4c-119">Det andra kommandot tar bort den virtuella dator rollen som lagras i $VMRole.</span><span class="sxs-lookup"><span data-stu-id="84c4c-119">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="84c4c-120">Med kommandot uppmanas du att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="84c4c-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="84c4c-121">Om den här rollen inte skapades med portalen måste användaren ange namnet på moln tjänsten.</span><span class="sxs-lookup"><span data-stu-id="84c4c-121">Assuming this virtual machine role was not created using the portal, the user needs to specify the cloud service name.</span></span>
<span data-ttu-id="84c4c-122">I det här fallet "ContosoCloudService02".</span><span class="sxs-lookup"><span data-stu-id="84c4c-122">In this case named "ContosoCloudService02".</span></span>

### <span data-ttu-id="84c4c-123">Exempel 3: ta bort en virtuell dator roll utan bekräftelse</span><span class="sxs-lookup"><span data-stu-id="84c4c-123">Example 3: Remove a virtual machine role without confirmation</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

<span data-ttu-id="84c4c-124">Det första kommandot får moln tjänsten med namnet ContosoVMRole03 med hjälp av cmdleten **Get-WAPackVMRole** och lagrar sedan objektet i variabeln $VMRole.</span><span class="sxs-lookup"><span data-stu-id="84c4c-124">The first command gets the cloud service named ContosoVMRole03 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="84c4c-125">Det andra kommandot tar bort den virtuella dator rollen som lagras i $VMRole.</span><span class="sxs-lookup"><span data-stu-id="84c4c-125">The second command removes the virtual machine role stored in $VMRole.</span></span>
<span data-ttu-id="84c4c-126">Det här kommandot innehåller parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="84c4c-126">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="84c4c-127">Du uppmanas inte att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="84c4c-127">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="84c4c-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84c4c-128">PARAMETERS</span></span>

### <span data-ttu-id="84c4c-129">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="84c4c-129">-CloudServiceName</span></span>
<span data-ttu-id="84c4c-130">Anger namnet på den virtuella datorns moln tjänst.</span><span class="sxs-lookup"><span data-stu-id="84c4c-130">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c4c-131">-Force</span><span class="sxs-lookup"><span data-stu-id="84c4c-131">-Force</span></span>
<span data-ttu-id="84c4c-132">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="84c4c-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c4c-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84c4c-133">-PassThru</span></span>
<span data-ttu-id="84c4c-134">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="84c4c-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84c4c-135">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="84c4c-135">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c4c-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="84c4c-136">-Profile</span></span>
<span data-ttu-id="84c4c-137">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="84c4c-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="84c4c-138">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="84c4c-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c4c-139">-VMRole</span><span class="sxs-lookup"><span data-stu-id="84c4c-139">-VMRole</span></span>
<span data-ttu-id="84c4c-140">Anger en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="84c4c-140">Specifies a virtual machine role.</span></span>
<span data-ttu-id="84c4c-141">Använd cmdleten **Get-WAPackVMRole** för att få en virtuell dator roll.</span><span class="sxs-lookup"><span data-stu-id="84c4c-141">To get a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84c4c-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84c4c-142">-Confirm</span></span>
<span data-ttu-id="84c4c-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84c4c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c4c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c4c-144">-WhatIf</span></span>
<span data-ttu-id="84c4c-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="84c4c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c4c-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="84c4c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c4c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c4c-147">CommonParameters</span></span>
<span data-ttu-id="84c4c-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84c4c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c4c-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84c4c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c4c-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84c4c-150">INPUTS</span></span>

## <span data-ttu-id="84c4c-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84c4c-151">OUTPUTS</span></span>

## <span data-ttu-id="84c4c-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84c4c-152">NOTES</span></span>

## <span data-ttu-id="84c4c-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84c4c-153">RELATED LINKS</span></span>

[<span data-ttu-id="84c4c-154">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="84c4c-154">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="84c4c-155">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="84c4c-155">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="84c4c-156">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="84c4c-156">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


