---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: b208d7c0e0db028f1b3242a70be508fbbc3788ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756691"
---
# <span data-ttu-id="fc827-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="fc827-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="fc827-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fc827-102">SYNOPSIS</span></span>
<span data-ttu-id="fc827-103">Hämtar krypterings statusen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fc827-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc827-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fc827-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc827-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fc827-105">DESCRIPTION</span></span>
<span data-ttu-id="fc827-106">Cmdleten **Get-AzureRmVMDiskEncryptionStatus** får den virtuella datorns krypterings status.</span><span class="sxs-lookup"><span data-stu-id="fc827-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="fc827-107">Här visas krypterings statusen för operativ system och data volymer.</span><span class="sxs-lookup"><span data-stu-id="fc827-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="fc827-108">Förutom krypterings status visar den också krypterings hemlighet-URL: en, nyckel krypterings nyckelns URL, resurs-ID: n för de **valv** där krypterings nyckel och nyckel krypterings nyckel för operativ system volymen finns.</span><span class="sxs-lookup"><span data-stu-id="fc827-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="fc827-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fc827-109">EXAMPLES</span></span>

### <span data-ttu-id="fc827-110">Exempel 1: få krypterings status för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="fc827-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="fc827-111">Det här kommandot får krypterings statusen för den virtuella datorn som heter VM001.</span><span class="sxs-lookup"><span data-stu-id="fc827-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="fc827-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fc827-112">PARAMETERS</span></span>

### <span data-ttu-id="fc827-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc827-113">-DefaultProfile</span></span>
<span data-ttu-id="fc827-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fc827-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc827-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="fc827-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="fc827-116">Tillägget utgivarens namn.</span><span class="sxs-lookup"><span data-stu-id="fc827-116">The extension publisher name.</span></span> <span data-ttu-id="fc827-117">Ange endast den här parametern om du vill åsidosätta standardvärdet för "Microsoft. Azure. Security".</span><span class="sxs-lookup"><span data-stu-id="fc827-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="fc827-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="fc827-118">-ExtensionType</span></span>
<span data-ttu-id="fc827-119">Fil tilläggs typen.</span><span class="sxs-lookup"><span data-stu-id="fc827-119">The extension type.</span></span> <span data-ttu-id="fc827-120">Ange den här parametern om du vill åsidosätta standardvärdet "AzureDiskEncryption" för Windows-VMs och "AzureDiskEncryptionForLinux" för Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="fc827-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="fc827-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="fc827-121">-Name</span></span>
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

### <span data-ttu-id="fc827-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc827-122">-ResourceGroupName</span></span>
<span data-ttu-id="fc827-123">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="fc827-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fc827-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="fc827-124">-VMName</span></span>
<span data-ttu-id="fc827-125">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="fc827-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="fc827-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc827-126">CommonParameters</span></span>
<span data-ttu-id="fc827-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc827-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc827-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc827-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc827-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fc827-129">INPUTS</span></span>

### <span data-ttu-id="fc827-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fc827-130">System.String</span></span>

## <span data-ttu-id="fc827-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fc827-131">OUTPUTS</span></span>

### <span data-ttu-id="fc827-132">Microsoft. Azure. commands. Compute. extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="fc827-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="fc827-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fc827-133">NOTES</span></span>

## <span data-ttu-id="fc827-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fc827-134">RELATED LINKS</span></span>

[<span data-ttu-id="fc827-135">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fc827-135">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="fc827-136">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fc827-136">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


