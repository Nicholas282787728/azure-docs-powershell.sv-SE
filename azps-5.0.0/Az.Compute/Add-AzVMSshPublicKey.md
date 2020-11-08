---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272743"
---
# <span data-ttu-id="b92b5-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="b92b5-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="b92b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b92b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b92b5-103">Lägger till de offentliga nycklarna för SSH för en virtuell dator när det bara skapas.</span><span class="sxs-lookup"><span data-stu-id="b92b5-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="b92b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b92b5-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b92b5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b92b5-105">DESCRIPTION</span></span>
<span data-ttu-id="b92b5-106">Cmdleten **Add-AzVMSshPublicKey** lägger till de offentliga nycklar som du kan använda för att ansluta till en virtuell dator med Linux via Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="b92b5-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="b92b5-107">Det går inte att använda det här när du har skapat en dator, om du försöker använda det när du har skapat en dator utan Update-AzVM, kommer fel meddelandet att visas om du använder kommandot med Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="b92b5-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="b92b5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b92b5-108">EXAMPLES</span></span>

### <span data-ttu-id="b92b5-109">Exempel 1: lägga till en offentlig nycklar på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="b92b5-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="b92b5-110">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="b92b5-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="b92b5-111">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="b92b5-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b92b5-112">Det andra kommandot lägger till den offentliga knappen till den plats på VirtualMachine07 som anger parametern Path.</span><span class="sxs-lookup"><span data-stu-id="b92b5-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="b92b5-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b92b5-113">PARAMETERS</span></span>

### <span data-ttu-id="b92b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b92b5-114">-DefaultProfile</span></span>
<span data-ttu-id="b92b5-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b92b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b92b5-116">-Data</span><span class="sxs-lookup"><span data-stu-id="b92b5-116">-KeyData</span></span>
<span data-ttu-id="b92b5-117">Anger grundläggande 64-kodning för en offentlig.</span><span class="sxs-lookup"><span data-stu-id="b92b5-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="b92b5-118">Du kan ansluta till en virtuell dator med Linux genom att använda SSH eller genom att använda den parameter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b92b5-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="b92b5-119">-Path</span><span class="sxs-lookup"><span data-stu-id="b92b5-119">-Path</span></span>
<span data-ttu-id="b92b5-120">Anger den fullständiga sökvägen till en fil, på den virtuella datorn, där denna cmdlet lagrar den offentliga SSH-tangenten.</span><span class="sxs-lookup"><span data-stu-id="b92b5-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="b92b5-121">Om filen redan finns lägger denna cmdlet till filen.</span><span class="sxs-lookup"><span data-stu-id="b92b5-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="b92b5-122">-VM</span><span class="sxs-lookup"><span data-stu-id="b92b5-122">-VM</span></span>
<span data-ttu-id="b92b5-123">Anger det virtuella dator objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="b92b5-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="b92b5-124">Använd cmdleten [Get-AzVM](./Get-AzVM.md) för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b92b5-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="b92b5-125">Du kan använda cmdleten [New-AzVMConfig](./New-AzVMConfig.md) för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="b92b5-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b92b5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b92b5-126">CommonParameters</span></span>
<span data-ttu-id="b92b5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b92b5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b92b5-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b92b5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b92b5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b92b5-129">INPUTS</span></span>

### <span data-ttu-id="b92b5-130">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b92b5-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b92b5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b92b5-131">System.String</span></span>

## <span data-ttu-id="b92b5-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b92b5-132">OUTPUTS</span></span>

### <span data-ttu-id="b92b5-133">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b92b5-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b92b5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b92b5-134">NOTES</span></span>

## <span data-ttu-id="b92b5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b92b5-135">RELATED LINKS</span></span>

[<span data-ttu-id="b92b5-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="b92b5-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="b92b5-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b92b5-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
