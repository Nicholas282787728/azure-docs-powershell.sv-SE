---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
ms.openlocfilehash: 667ebae58974b2dc68d19daa6a4f3a9d2e98075d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928917"
---
# <span data-ttu-id="66040-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="66040-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="66040-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66040-102">SYNOPSIS</span></span>
<span data-ttu-id="66040-103">Hämtar krypterings statusen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="66040-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66040-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66040-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66040-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66040-105">DESCRIPTION</span></span>
<span data-ttu-id="66040-106">Cmdleten **Get-AzureRmVMDiskEncryptionStatus** får den virtuella datorns krypterings status.</span><span class="sxs-lookup"><span data-stu-id="66040-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="66040-107">Här visas krypterings statusen för operativ system och data volymer.</span><span class="sxs-lookup"><span data-stu-id="66040-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="66040-108">Förutom krypterings status visar den också krypterings hemlighet-URL: en, nyckel krypterings nyckelns URL, resurs-ID: n för de **valv** där krypterings nyckel och nyckel krypterings nyckel för operativ system volymen finns.</span><span class="sxs-lookup"><span data-stu-id="66040-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="66040-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66040-109">EXAMPLES</span></span>

### <span data-ttu-id="66040-110">Exempel 1: få krypterings status för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="66040-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="66040-111">Det här kommandot får krypterings statusen för den virtuella datorn som heter VM001.</span><span class="sxs-lookup"><span data-stu-id="66040-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="66040-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66040-112">PARAMETERS</span></span>

### <span data-ttu-id="66040-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66040-113">-DefaultProfile</span></span>
<span data-ttu-id="66040-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66040-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66040-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="66040-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="66040-116">Tillägget utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="66040-116">The extension publisher name.</span></span> <span data-ttu-id="66040-117">Ange endast den här parametern om du vill åsidosätta standardvärdet för "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="66040-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66040-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="66040-118">-ExtensionType</span></span>
<span data-ttu-id="66040-119">Fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="66040-119">The extension type.</span></span> <span data-ttu-id="66040-120">Ange den här parametern om du vill åsidosätta standardvärdet "AzureDiskEncryption" för Windows-VMs och "AzureDiskEncryptionForLinux" för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="66040-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66040-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="66040-121">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66040-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66040-122">-ResourceGroupName</span></span>
<span data-ttu-id="66040-123">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="66040-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66040-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="66040-124">-VMName</span></span>
<span data-ttu-id="66040-125">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="66040-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66040-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66040-126">CommonParameters</span></span>
<span data-ttu-id="66040-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66040-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66040-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66040-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66040-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66040-129">INPUTS</span></span>

### <span data-ttu-id="66040-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="66040-130">None</span></span>
<span data-ttu-id="66040-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="66040-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66040-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66040-132">OUTPUTS</span></span>

### <span data-ttu-id="66040-133">Microsoft. Azure. commands. Compute. extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="66040-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="66040-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66040-134">NOTES</span></span>

## <span data-ttu-id="66040-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66040-135">RELATED LINKS</span></span>

[<span data-ttu-id="66040-136">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="66040-136">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="66040-137">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="66040-137">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


