---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 6ca619ba75fcf639e36650dc66d45d2f86ec8375
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757717"
---
# <span data-ttu-id="de992-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="de992-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="de992-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="de992-102">SYNOPSIS</span></span>
<span data-ttu-id="de992-103">Lägger till offentliga nycklar för SSH till VMSS.</span><span class="sxs-lookup"><span data-stu-id="de992-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de992-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="de992-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de992-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="de992-105">DESCRIPTION</span></span>
<span data-ttu-id="de992-106">Cmdleten **Add-AzureRmVmssSshPublicKey** lägger till de offentliga nycklar som du kan använda för att ansluta till virtuella datorer med VMSS (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="de992-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="de992-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="de992-107">EXAMPLES</span></span>

### <span data-ttu-id="de992-108">Exempel 1: lägga till en offentlig SSH-VMSS</span><span class="sxs-lookup"><span data-stu-id="de992-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="de992-109">Det här exemplet lägger till en offentlig SSH-VMSS.</span><span class="sxs-lookup"><span data-stu-id="de992-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="de992-110">I det första kommandot används cmdleten **New-AzureRmVmssConfig** för att skapa ett VMSS-konfigurationsobjekt och det lagrar resultatet i variabeln som heter $VMSS.</span><span class="sxs-lookup"><span data-stu-id="de992-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="de992-111">Det andra kommandot lägger till en SSH-nyckel med de angivna nyckel data och lagrar den på den angivna sökvägen på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="de992-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="de992-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="de992-112">PARAMETERS</span></span>

### <span data-ttu-id="de992-113">-Data</span><span class="sxs-lookup"><span data-stu-id="de992-113">-KeyData</span></span>
<span data-ttu-id="de992-114">Anger information om offentliga nycklar för SSH RSA.</span><span class="sxs-lookup"><span data-stu-id="de992-114">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de992-115">-Path</span><span class="sxs-lookup"><span data-stu-id="de992-115">-Path</span></span>
<span data-ttu-id="de992-116">Anger den fullständiga sökvägen till en fil, på den virtuella datorn, där denna cmdlet lagrar den offentliga SSH-tangenten.</span><span class="sxs-lookup"><span data-stu-id="de992-116">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="de992-117">Om filen redan finns lägger denna cmdlet till filen.</span><span class="sxs-lookup"><span data-stu-id="de992-117">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de992-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="de992-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="de992-119">Anger VMSS-objektet.</span><span class="sxs-lookup"><span data-stu-id="de992-119">Specifies the VMSS object.</span></span>
<span data-ttu-id="de992-120">Du kan använda cmdleten [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) för att skapa objektet.</span><span class="sxs-lookup"><span data-stu-id="de992-120">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de992-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="de992-121">-Confirm</span></span>
<span data-ttu-id="de992-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="de992-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de992-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de992-123">-WhatIf</span></span>
<span data-ttu-id="de992-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="de992-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de992-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="de992-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de992-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de992-126">CommonParameters</span></span>
<span data-ttu-id="de992-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de992-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de992-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de992-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de992-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="de992-129">INPUTS</span></span>

### <span data-ttu-id="de992-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="de992-130">None</span></span>
<span data-ttu-id="de992-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="de992-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de992-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="de992-132">OUTPUTS</span></span>

###  
<span data-ttu-id="de992-133">Denna cmdlet genererar inga utdata.</span><span class="sxs-lookup"><span data-stu-id="de992-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="de992-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="de992-134">NOTES</span></span>

## <span data-ttu-id="de992-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="de992-135">RELATED LINKS</span></span>

[<span data-ttu-id="de992-136">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="de992-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)