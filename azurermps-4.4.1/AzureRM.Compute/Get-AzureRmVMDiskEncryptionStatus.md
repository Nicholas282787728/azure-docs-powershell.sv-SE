---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 0d7312d7ecbddf15530438e9729e470bd202e488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756630"
---
# <span data-ttu-id="582b2-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="582b2-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="582b2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="582b2-102">SYNOPSIS</span></span>
<span data-ttu-id="582b2-103">Hämtar krypterings statusen för den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="582b2-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="582b2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="582b2-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="582b2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="582b2-105">DESCRIPTION</span></span>
<span data-ttu-id="582b2-106">Cmdleten **Get-AzureRmVMDiskEncryptionStatus** får den virtuella datorns krypterings status.</span><span class="sxs-lookup"><span data-stu-id="582b2-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="582b2-107">Här visas krypterings statusen för operativ system och data volymer.</span><span class="sxs-lookup"><span data-stu-id="582b2-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="582b2-108">Förutom krypterings status visar den också krypterings hemlighet-URL: en, nyckel krypterings nyckelns URL, resurs-ID: n för de **valv** där krypterings nyckel och nyckel krypterings nyckel för operativ system volymen finns.</span><span class="sxs-lookup"><span data-stu-id="582b2-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="582b2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="582b2-109">EXAMPLES</span></span>

### <span data-ttu-id="582b2-110">Exempel 1: få krypterings status för en virtuell dator</span><span class="sxs-lookup"><span data-stu-id="582b2-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="582b2-111">Det här kommandot får krypterings statusen för den virtuella datorn som heter VM001.</span><span class="sxs-lookup"><span data-stu-id="582b2-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="582b2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="582b2-112">PARAMETERS</span></span>

### <span data-ttu-id="582b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="582b2-113">-DefaultProfile</span></span>
<span data-ttu-id="582b2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="582b2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="582b2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="582b2-115">-Name</span></span>
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

### <span data-ttu-id="582b2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="582b2-116">-ResourceGroupName</span></span>
<span data-ttu-id="582b2-117">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="582b2-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="582b2-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="582b2-118">-VMName</span></span>
<span data-ttu-id="582b2-119">Anger namnet på den virtuella datorn.</span><span class="sxs-lookup"><span data-stu-id="582b2-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="582b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="582b2-120">CommonParameters</span></span>
<span data-ttu-id="582b2-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="582b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="582b2-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="582b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="582b2-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="582b2-123">INPUTS</span></span>

## <span data-ttu-id="582b2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="582b2-124">OUTPUTS</span></span>

## <span data-ttu-id="582b2-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="582b2-125">NOTES</span></span>

## <span data-ttu-id="582b2-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="582b2-126">RELATED LINKS</span></span>

[<span data-ttu-id="582b2-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="582b2-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="582b2-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="582b2-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


