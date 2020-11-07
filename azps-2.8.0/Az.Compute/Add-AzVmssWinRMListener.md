---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 79d6a48ca2c6f86b84e8f02514191a2e4815f350
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745225"
---
# <span data-ttu-id="2c714-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="2c714-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="2c714-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c714-102">SYNOPSIS</span></span>
<span data-ttu-id="2c714-103">Lägger till en WinRM-lyssnare till VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c714-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="2c714-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c714-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c714-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c714-105">DESCRIPTION</span></span>
<span data-ttu-id="2c714-106">Cmdleten **Add-AzVmssWinRMListener** lägger till en WinRM-lyssnare (Windows Remote Management) på den virtuella datorns skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="2c714-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="2c714-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c714-107">EXAMPLES</span></span>

### <span data-ttu-id="2c714-108">Exempel 1: lägga till en WinRM-lyssnare i VMSS</span><span class="sxs-lookup"><span data-stu-id="2c714-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="2c714-109">Det här exemplet lägger till en WinRM-lyssnare till VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c714-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="2c714-110">I det första kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c714-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="2c714-111">Det andra kommandot lägger till ett HTTP-protokoll WinRM-lyssnare med certifikatet på den angivna URL-adressen till VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c714-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="2c714-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c714-112">PARAMETERS</span></span>

### <span data-ttu-id="2c714-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="2c714-113">-CertificateUrl</span></span>
<span data-ttu-id="2c714-114">Anger en länk, som en URL, för det certifikat som de nya virtuella datorerna etableras med.</span><span class="sxs-lookup"><span data-stu-id="2c714-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c714-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c714-115">-DefaultProfile</span></span>
<span data-ttu-id="2c714-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c714-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c714-117">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2c714-117">-Protocol</span></span>
<span data-ttu-id="2c714-118">Anger protokollet för WinRM-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="2c714-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="2c714-119">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2c714-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c714-120">Inkommande</span><span class="sxs-lookup"><span data-stu-id="2c714-120">Http</span></span>
- <span data-ttu-id="2c714-121">Https</span><span class="sxs-lookup"><span data-stu-id="2c714-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c714-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c714-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2c714-123">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="2c714-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="2c714-124">Du kan använda New-AzVmssConfig-cmdleten för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="2c714-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c714-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2c714-125">-Confirm</span></span>
<span data-ttu-id="2c714-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2c714-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c714-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c714-127">-WhatIf</span></span>
<span data-ttu-id="2c714-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2c714-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c714-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2c714-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c714-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c714-130">CommonParameters</span></span>
<span data-ttu-id="2c714-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c714-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c714-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c714-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c714-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c714-133">INPUTS</span></span>

### <span data-ttu-id="2c714-134">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c714-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2c714-135">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ProtocolTypes, Microsoft. Azure. Management. Compute, version = 23.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2c714-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2c714-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2c714-136">System.String</span></span>

## <span data-ttu-id="2c714-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c714-137">OUTPUTS</span></span>

### <span data-ttu-id="2c714-138">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c714-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2c714-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c714-139">NOTES</span></span>

## <span data-ttu-id="2c714-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c714-140">RELATED LINKS</span></span>

[<span data-ttu-id="2c714-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2c714-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

