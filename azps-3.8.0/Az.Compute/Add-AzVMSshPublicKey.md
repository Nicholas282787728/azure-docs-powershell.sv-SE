---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: dfbb993e0753ab536fa1daf54024facf8fed1624
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091172"
---
# <span data-ttu-id="e8763-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e8763-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="e8763-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8763-102">SYNOPSIS</span></span>
<span data-ttu-id="e8763-103">Lägger till de offentliga nycklarna för SSH för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e8763-103">Adds the public keys for SSH for a virtual machine.</span></span>

## <span data-ttu-id="e8763-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8763-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8763-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8763-105">DESCRIPTION</span></span>
<span data-ttu-id="e8763-106">Cmdleten **Add-AzVMSshPublicKey** lägger till de offentliga nycklar som du kan använda för att ansluta till en virtuell dator med Linux via Secure Shell (SSH).</span><span class="sxs-lookup"><span data-stu-id="e8763-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="e8763-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8763-107">EXAMPLES</span></span>

### <span data-ttu-id="e8763-108">Exempel 1: lägga till en offentlig nycklar på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="e8763-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="e8763-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="e8763-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="e8763-110">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="e8763-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e8763-111">Det andra kommandot lägger till den offentliga knappen till den plats på VirtualMachine07 som anger parametern Path.</span><span class="sxs-lookup"><span data-stu-id="e8763-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="e8763-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8763-112">PARAMETERS</span></span>

### <span data-ttu-id="e8763-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8763-113">-DefaultProfile</span></span>
<span data-ttu-id="e8763-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8763-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8763-115">-Data</span><span class="sxs-lookup"><span data-stu-id="e8763-115">-KeyData</span></span>
<span data-ttu-id="e8763-116">Anger grundläggande 64-kodning för en offentlig.</span><span class="sxs-lookup"><span data-stu-id="e8763-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="e8763-117">Du kan ansluta till en virtuell dator med Linux genom att använda SSH eller genom att använda den parameter som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="e8763-117">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="e8763-118">-Path</span><span class="sxs-lookup"><span data-stu-id="e8763-118">-Path</span></span>
<span data-ttu-id="e8763-119">Anger den fullständiga sökvägen till en fil, på den virtuella datorn, där denna cmdlet lagrar den offentliga SSH-tangenten.</span><span class="sxs-lookup"><span data-stu-id="e8763-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="e8763-120">Om filen redan finns lägger denna cmdlet till filen.</span><span class="sxs-lookup"><span data-stu-id="e8763-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="e8763-121">-VM</span><span class="sxs-lookup"><span data-stu-id="e8763-121">-VM</span></span>
<span data-ttu-id="e8763-122">Anger det virtuella dator objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="e8763-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="e8763-123">Använd cmdleten [Get-AzVM](./Get-AzVM.md) för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e8763-123">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="e8763-124">Du kan använda cmdleten [New-AzVMConfig](./New-AzVMConfig.md) för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="e8763-124">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="e8763-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8763-125">CommonParameters</span></span>
<span data-ttu-id="e8763-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8763-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8763-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8763-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8763-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8763-128">INPUTS</span></span>

### <span data-ttu-id="e8763-129">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e8763-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e8763-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8763-130">System.String</span></span>

## <span data-ttu-id="e8763-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8763-131">OUTPUTS</span></span>

### <span data-ttu-id="e8763-132">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e8763-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e8763-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8763-133">NOTES</span></span>

## <span data-ttu-id="e8763-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8763-134">RELATED LINKS</span></span>

[<span data-ttu-id="e8763-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e8763-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e8763-136">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e8763-136">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
