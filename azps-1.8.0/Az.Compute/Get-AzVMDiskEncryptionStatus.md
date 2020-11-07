---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 1b2a3855703c1d91a17cfd164f6a65ce218da486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917441"
---
# <span data-ttu-id="d7f82-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d7f82-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="d7f82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d7f82-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f82-103">Hämtar krypterings statusen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d7f82-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="d7f82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d7f82-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7f82-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d7f82-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f82-106">Cmdleten **Get-AzVMDiskEncryptionStatus** får den virtuella datorns krypterings status.</span><span class="sxs-lookup"><span data-stu-id="d7f82-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="d7f82-107">Här visas krypterings statusen för operativ system och data volymer.</span><span class="sxs-lookup"><span data-stu-id="d7f82-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="d7f82-108">Förutom krypterings status visar den också krypterings hemlighet-URL: en, nyckel krypterings nyckelns URL, resurs-ID: n för de **valv** där krypterings nyckel och nyckel krypterings nyckel för operativ system volymen finns.</span><span class="sxs-lookup"><span data-stu-id="d7f82-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="d7f82-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d7f82-109">EXAMPLES</span></span>

### <span data-ttu-id="d7f82-110">Exempel 1: få krypterings status för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="d7f82-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="d7f82-111">Det här kommandot får krypterings statusen för den virtuella datorn som heter VM001.</span><span class="sxs-lookup"><span data-stu-id="d7f82-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="d7f82-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d7f82-112">PARAMETERS</span></span>

### <span data-ttu-id="d7f82-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f82-113">-DefaultProfile</span></span>
<span data-ttu-id="d7f82-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f82-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7f82-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="d7f82-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="d7f82-116">Tillägget utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="d7f82-116">The extension publisher name.</span></span> <span data-ttu-id="d7f82-117">Ange endast den här parametern om du vill åsidosätta standardvärdet för "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="d7f82-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f82-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d7f82-118">-ExtensionType</span></span>
<span data-ttu-id="d7f82-119">Fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="d7f82-119">The extension type.</span></span> <span data-ttu-id="d7f82-120">Ange den här parametern om du vill åsidosätta standardvärdet "AzureDiskEncryption" för Windows-VMs och "AzureDiskEncryptionForLinux" för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="d7f82-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f82-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d7f82-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f82-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f82-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7f82-123">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d7f82-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f82-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d7f82-124">-VMName</span></span>
<span data-ttu-id="d7f82-125">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="d7f82-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f82-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f82-126">CommonParameters</span></span>
<span data-ttu-id="d7f82-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f82-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f82-128">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7f82-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f82-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d7f82-129">INPUTS</span></span>

### <span data-ttu-id="d7f82-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d7f82-130">System.String</span></span>

## <span data-ttu-id="d7f82-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d7f82-131">OUTPUTS</span></span>

### <span data-ttu-id="d7f82-132">Microsoft. Azure. commands. Compute. extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d7f82-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="d7f82-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d7f82-133">NOTES</span></span>

## <span data-ttu-id="d7f82-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d7f82-134">RELATED LINKS</span></span>

[<span data-ttu-id="d7f82-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d7f82-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="d7f82-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d7f82-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


