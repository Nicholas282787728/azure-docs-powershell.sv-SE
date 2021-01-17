---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402011"
---
# <span data-ttu-id="70ff4-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="70ff4-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="70ff4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="70ff4-103">Lägger till offentliga nycklar för SSH till VMSS.</span><span class="sxs-lookup"><span data-stu-id="70ff4-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="70ff4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70ff4-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70ff4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="70ff4-106">Cmdleten **Add-AzVmssSshPublicKey** lägger till de offentliga nycklar som du kan använda för att ansluta till virtuella datorer med VMSS (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="70ff4-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="70ff4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70ff4-107">EXAMPLES</span></span>

### <span data-ttu-id="70ff4-108">Exempel 1: lägga till en offentlig SSH-VMSS</span><span class="sxs-lookup"><span data-stu-id="70ff4-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="70ff4-109">Det här exemplet lägger till en offentlig SSH-VMSS.</span><span class="sxs-lookup"><span data-stu-id="70ff4-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="70ff4-110">I det första kommandot används cmdleten **New-AzVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="70ff4-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="70ff4-111">Det andra kommandot lägger till en SSH-nyckel med de angivna nyckel data och lagrar den på den angivna sökvägen på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="70ff4-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="70ff4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70ff4-112">PARAMETERS</span></span>

### <span data-ttu-id="70ff4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ff4-113">-DefaultProfile</span></span>
<span data-ttu-id="70ff4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70ff4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70ff4-115">-Data</span><span class="sxs-lookup"><span data-stu-id="70ff4-115">-KeyData</span></span>
<span data-ttu-id="70ff4-116">Anger information om offentliga nycklar för SSH RSA.</span><span class="sxs-lookup"><span data-stu-id="70ff4-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="70ff4-117">-Path</span><span class="sxs-lookup"><span data-stu-id="70ff4-117">-Path</span></span>
<span data-ttu-id="70ff4-118">Anger den fullständiga sökvägen till en fil, på den virtuella datorn, där denna cmdlet lagrar den offentliga SSH-tangenten.</span><span class="sxs-lookup"><span data-stu-id="70ff4-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="70ff4-119">Om filen redan finns lägger denna cmdlet till filen.</span><span class="sxs-lookup"><span data-stu-id="70ff4-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ff4-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70ff4-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="70ff4-121">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="70ff4-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="70ff4-122">Du kan använda cmdleten [New-AzVmssConfig](./New-AzVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="70ff4-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="70ff4-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70ff4-123">-Confirm</span></span>
<span data-ttu-id="70ff4-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70ff4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ff4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ff4-125">-WhatIf</span></span>
<span data-ttu-id="70ff4-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70ff4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70ff4-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70ff4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ff4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ff4-128">CommonParameters</span></span>
<span data-ttu-id="70ff4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ff4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ff4-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70ff4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ff4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70ff4-131">INPUTS</span></span>

### <span data-ttu-id="70ff4-132">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70ff4-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="70ff4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="70ff4-133">System.String</span></span>

## <span data-ttu-id="70ff4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70ff4-134">OUTPUTS</span></span>

### <span data-ttu-id="70ff4-135">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="70ff4-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="70ff4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70ff4-136">NOTES</span></span>

## <span data-ttu-id="70ff4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70ff4-137">RELATED LINKS</span></span>

[<span data-ttu-id="70ff4-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="70ff4-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
