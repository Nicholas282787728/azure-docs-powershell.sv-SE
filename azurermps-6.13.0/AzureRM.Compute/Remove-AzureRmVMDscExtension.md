---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b25b65e9c42cd388d685320802690c6538122e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573994"
---
# <span data-ttu-id="62330-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62330-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="62330-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="62330-102">SYNOPSIS</span></span>
<span data-ttu-id="62330-103">Tar bort en DSC-tilläggsprovider från en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62330-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62330-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="62330-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62330-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="62330-105">DESCRIPTION</span></span>
<span data-ttu-id="62330-106">Cmdleten **Remove-AzureRmVMDscExtension** tar bort en fil tilläggs hanterare för önskad tillstånds konfiguration (DSC) från en virtuell dator i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62330-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="62330-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="62330-107">EXAMPLES</span></span>

### <span data-ttu-id="62330-108">Exempel 1: ta bort ett DSC-tillägg</span><span class="sxs-lookup"><span data-stu-id="62330-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="62330-109">Det här kommandot tar bort tillägget DSC på den virtuella datorn med namnet VM07.</span><span class="sxs-lookup"><span data-stu-id="62330-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="62330-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="62330-110">PARAMETERS</span></span>

### <span data-ttu-id="62330-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62330-111">-DefaultProfile</span></span>
<span data-ttu-id="62330-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="62330-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62330-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="62330-113">-Name</span></span>
<span data-ttu-id="62330-114">Anger namnet på det DSC-tillägg som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="62330-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="62330-115">Set-AzureRmVMDscExtension cmdlet anger det här namnet till Microsoft. PowerShell. DSC, vilket är det standardvärde som används av **Remove-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="62330-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

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

### <span data-ttu-id="62330-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62330-116">-ResourceGroupName</span></span>
<span data-ttu-id="62330-117">Anger namnet på den virtuella datorns resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="62330-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="62330-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="62330-118">-VMName</span></span>
<span data-ttu-id="62330-119">Anger namnet på en virtuell dator från vilken denna cmdlet tar bort DSC-tillägget.</span><span class="sxs-lookup"><span data-stu-id="62330-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62330-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="62330-120">-Confirm</span></span>
<span data-ttu-id="62330-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="62330-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62330-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62330-122">-WhatIf</span></span>
<span data-ttu-id="62330-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="62330-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62330-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="62330-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62330-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62330-125">CommonParameters</span></span>
<span data-ttu-id="62330-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62330-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62330-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62330-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62330-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="62330-128">INPUTS</span></span>

### <span data-ttu-id="62330-129">System. String</span><span class="sxs-lookup"><span data-stu-id="62330-129">System.String</span></span>

## <span data-ttu-id="62330-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="62330-130">OUTPUTS</span></span>

### <span data-ttu-id="62330-131">Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="62330-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="62330-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="62330-132">NOTES</span></span>

## <span data-ttu-id="62330-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="62330-133">RELATED LINKS</span></span>

[<span data-ttu-id="62330-134">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62330-134">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="62330-135">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62330-135">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


