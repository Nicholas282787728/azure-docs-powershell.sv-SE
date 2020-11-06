---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581456"
---
# <span data-ttu-id="a5ac2-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5ac2-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="a5ac2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ac2-103">Tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5ac2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5ac2-104">SYNTAX</span></span>

### <span data-ttu-id="a5ac2-105">ResourceGroupNameParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="a5ac2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ac2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a5ac2-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ac2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5ac2-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ac2-108">Cmdleten **Remove-AzureRmVM** tar bort en virtuell dator från Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="a5ac2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5ac2-109">EXAMPLES</span></span>

### <span data-ttu-id="a5ac2-110">Exempel 1: ta bort en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="a5ac2-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="a5ac2-111">Det här kommandot tar bort den virtuella datorn med namnet VirtualMachine07 i resurs gruppen ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="a5ac2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5ac2-112">PARAMETERS</span></span>

### <span data-ttu-id="a5ac2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ac2-113">-DefaultProfile</span></span>
<span data-ttu-id="a5ac2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5ac2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5ac2-115">-Force</span></span>
<span data-ttu-id="a5ac2-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5ac2-117">-ID</span><span class="sxs-lookup"><span data-stu-id="a5ac2-117">-Id</span></span>
<span data-ttu-id="a5ac2-118">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ac2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5ac2-119">-Name</span></span>
<span data-ttu-id="a5ac2-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ac2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ac2-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5ac2-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5ac2-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5ac2-123">-Confirm</span></span>
<span data-ttu-id="a5ac2-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ac2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ac2-125">-WhatIf</span></span>
<span data-ttu-id="a5ac2-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a5ac2-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ac2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ac2-128">CommonParameters</span></span>
<span data-ttu-id="a5ac2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ac2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5ac2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ac2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5ac2-131">INPUTS</span></span>

## <span data-ttu-id="a5ac2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5ac2-132">OUTPUTS</span></span>

## <span data-ttu-id="a5ac2-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5ac2-133">NOTES</span></span>

## <span data-ttu-id="a5ac2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5ac2-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5ac2-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5ac2-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a5ac2-136">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5ac2-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="a5ac2-137">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5ac2-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="a5ac2-138">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5ac2-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="a5ac2-139">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5ac2-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="a5ac2-140">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a5ac2-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


