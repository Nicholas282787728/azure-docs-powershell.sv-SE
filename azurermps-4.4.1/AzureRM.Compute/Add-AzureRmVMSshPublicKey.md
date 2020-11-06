---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 24c97e73728dab656a1d9fe3283e4eba6aae4ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573732"
---
# <span data-ttu-id="88155-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="88155-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="88155-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="88155-102">SYNOPSIS</span></span>
<span data-ttu-id="88155-103">Lägger till de offentliga nycklarna för SSH för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="88155-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88155-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="88155-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88155-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="88155-105">DESCRIPTION</span></span>
<span data-ttu-id="88155-106">Cmdleten **Add-AzureRmVMSshPublicKey** lägger till de offentliga nycklar som du kan använda för att ansluta till en virtuell dator via SSH (Secure Shell).</span><span class="sxs-lookup"><span data-stu-id="88155-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="88155-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="88155-107">EXAMPLES</span></span>

### <span data-ttu-id="88155-108">Exempel 1: lägga till en offentlig nycklar på en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="88155-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="88155-109">Det första kommandot får den virtuella datorn som heter VirtualMachine07 med hjälp av cmdleten **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="88155-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="88155-110">Kommandot lagrar den virtuella datorn i $VirtualMachine variabel.</span><span class="sxs-lookup"><span data-stu-id="88155-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="88155-111">Det andra kommandot lägger till den offentliga knappen till den plats på VirtualMachine07 som anger parametern Path.</span><span class="sxs-lookup"><span data-stu-id="88155-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="88155-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="88155-112">PARAMETERS</span></span>

### <span data-ttu-id="88155-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88155-113">-DefaultProfile</span></span>
<span data-ttu-id="88155-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="88155-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88155-115">-Data</span><span class="sxs-lookup"><span data-stu-id="88155-115">-KeyData</span></span>
<span data-ttu-id="88155-116">Anger grundläggande 64-kodning för en offentlig.</span><span class="sxs-lookup"><span data-stu-id="88155-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="88155-117">Du kan ansluta till en virtuell dator med hjälp av SSH eller genom att använda en av de nycklar som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="88155-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="88155-118">-Path</span><span class="sxs-lookup"><span data-stu-id="88155-118">-Path</span></span>
<span data-ttu-id="88155-119">Anger den fullständiga sökvägen till en fil, på den virtuella datorn, där denna cmdlet lagrar den offentliga SSH-tangenten.</span><span class="sxs-lookup"><span data-stu-id="88155-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="88155-120">Om filen redan finns lägger denna cmdlet till filen.</span><span class="sxs-lookup"><span data-stu-id="88155-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="88155-121">-VM</span><span class="sxs-lookup"><span data-stu-id="88155-121">-VM</span></span>
<span data-ttu-id="88155-122">Anger det virtuella dator objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="88155-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="88155-123">Använd cmdleten [Get-AzureRmVM](./Get-AzureRmVM.md) för att hämta ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="88155-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="88155-124">Du kan använda cmdleten [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) för att skapa ett virtuellt dator objekt.</span><span class="sxs-lookup"><span data-stu-id="88155-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="88155-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88155-125">CommonParameters</span></span>
<span data-ttu-id="88155-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88155-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88155-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88155-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88155-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="88155-128">INPUTS</span></span>

## <span data-ttu-id="88155-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="88155-129">OUTPUTS</span></span>

## <span data-ttu-id="88155-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="88155-130">NOTES</span></span>

## <span data-ttu-id="88155-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="88155-131">RELATED LINKS</span></span>

[<span data-ttu-id="88155-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="88155-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="88155-133">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="88155-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
