---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsshpublickey
schema: 2.0.0
ms.openlocfilehash: c8109a1fa13bff2a2a527bb7e1f9cb232d0e61c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930750"
---
# <span data-ttu-id="ba4d6-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ba4d6-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="ba4d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba4d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4d6-103">Lägger till de offentliga nycklarna för SSH för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba4d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba4d6-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba4d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba4d6-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4d6-106">Cmdleten **Add-AzureRmVMSshPublicKey** lägger till de offentliga nycklar som du kan använda för att ansluta till en virtuell dator via SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="ba4d6-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="ba4d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba4d6-107">EXAMPLES</span></span>

### <span data-ttu-id="ba4d6-108">Exempel 1: lägga till en offentlig nycklar på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="ba4d6-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="ba4d6-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="ba4d6-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="ba4d6-110">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ba4d6-111">Det andra kommandot lägger till den offentliga knappen till den plats på VirtualMachine07 som anger parametern Path.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="ba4d6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba4d6-112">PARAMETERS</span></span>

### <span data-ttu-id="ba4d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4d6-113">-DefaultProfile</span></span>
<span data-ttu-id="ba4d6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4d6-115">-Data</span><span class="sxs-lookup"><span data-stu-id="ba4d6-115">-KeyData</span></span>
<span data-ttu-id="ba4d6-116">Anger grundläggande 64-kodning för en offentlig.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="ba4d6-117">Du kan ansluta till en virtuell dator med hjälp av SSH eller genom att använda en av de nycklar som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="ba4d6-118">-Path</span><span class="sxs-lookup"><span data-stu-id="ba4d6-118">-Path</span></span>
<span data-ttu-id="ba4d6-119">Anger den fullständiga sökvägen till en fil, på den virtuella datorn, där denna cmdlet lagrar den offentliga SSH-tangenten.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="ba4d6-120">Om filen redan finns lägger denna cmdlet till filen.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="ba4d6-121">-VM</span><span class="sxs-lookup"><span data-stu-id="ba4d6-121">-VM</span></span>
<span data-ttu-id="ba4d6-122">Anger det virtuella dator objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="ba4d6-123">Använd cmdleten [Get-AzureRmVM](./Get-AzureRmVM.md) för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="ba4d6-124">Du kan använda cmdleten [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba4d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4d6-125">CommonParameters</span></span>
<span data-ttu-id="ba4d6-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba4d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4d6-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4d6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4d6-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba4d6-128">INPUTS</span></span>

### <span data-ttu-id="ba4d6-129">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ba4d6-129">PSVirtualMachine</span></span>
<span data-ttu-id="ba4d6-130">Parametern ' VM ' godkänner värdet av typen ' PSVirtualMachine ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="ba4d6-130">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ba4d6-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba4d6-131">OUTPUTS</span></span>

### <span data-ttu-id="ba4d6-132">Microsoft. Azure. commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ba4d6-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ba4d6-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba4d6-133">NOTES</span></span>

## <span data-ttu-id="ba4d6-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba4d6-134">RELATED LINKS</span></span>

[<span data-ttu-id="ba4d6-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ba4d6-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ba4d6-136">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ba4d6-136">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
