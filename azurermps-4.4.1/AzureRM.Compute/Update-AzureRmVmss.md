---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 44022fe8ea12c8f341952bd023aa41bf4ead92c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579752"
---
# <span data-ttu-id="452be-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="452be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="452be-102">SYNOPSIS</span></span>
<span data-ttu-id="452be-103">Uppdaterar tillståndet för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="452be-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="452be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="452be-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="452be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="452be-105">DESCRIPTION</span></span>
<span data-ttu-id="452be-106">Cmdleten **Update-AzureRmVmss** uppdaterar tillståndet för en virtuell dators skalnings uppsättning (VMSS) till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="452be-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="452be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="452be-107">EXAMPLES</span></span>

### <span data-ttu-id="452be-108">Exempel 1: Uppdatera statusen för en VMSS till tillståndet för ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="452be-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="452be-109">Det här kommandot uppdaterar tillståndet för VMSS med namnet VMSS001 som tillhör resurs gruppen som heter Group001 till statusen för ett lokalt VMSS-objekt med namnet LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="452be-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="452be-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="452be-110">PARAMETERS</span></span>

### <span data-ttu-id="452be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452be-111">-DefaultProfile</span></span>
<span data-ttu-id="452be-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="452be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="452be-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452be-113">-ResourceGroupName</span></span>
<span data-ttu-id="452be-114">Anger namnet på den resurs grupp som VMSS tillhör.</span><span class="sxs-lookup"><span data-stu-id="452be-114">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="452be-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="452be-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="452be-116">Anger ett lokalt VMSS-objekt.</span><span class="sxs-lookup"><span data-stu-id="452be-116">Specifies a local VMSS object.</span></span>
<span data-ttu-id="452be-117">För att hämta ett VMSS-objekt, Använd cmdleten Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="452be-117">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="452be-118">Det här virtuella dator objektet innehåller det uppdaterade tillståndet för VMSS.</span><span class="sxs-lookup"><span data-stu-id="452be-118">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="452be-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="452be-119">-VMScaleSetName</span></span>
<span data-ttu-id="452be-120">Anger namnet på den VMSS som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="452be-120">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="452be-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="452be-121">-Confirm</span></span>
<span data-ttu-id="452be-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="452be-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="452be-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="452be-123">-WhatIf</span></span>
<span data-ttu-id="452be-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="452be-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="452be-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="452be-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="452be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452be-126">CommonParameters</span></span>
<span data-ttu-id="452be-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="452be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452be-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="452be-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452be-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="452be-129">INPUTS</span></span>

## <span data-ttu-id="452be-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="452be-130">OUTPUTS</span></span>

## <span data-ttu-id="452be-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="452be-131">NOTES</span></span>

## <span data-ttu-id="452be-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="452be-132">RELATED LINKS</span></span>

[<span data-ttu-id="452be-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="452be-134">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="452be-135">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="452be-136">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="452be-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="452be-138">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="452be-139">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="452be-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


