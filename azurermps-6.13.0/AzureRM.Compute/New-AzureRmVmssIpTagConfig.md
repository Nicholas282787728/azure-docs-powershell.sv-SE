---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVmssIpTagConfig.md
ms.openlocfilehash: a77680921eeef0a678cbd83d04bef9a51cf35cb3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572895"
---
# <span data-ttu-id="f9ed5-101">New-AzureRmVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="f9ed5-101">New-AzureRmVmssIpTagConfig</span></span>

## <span data-ttu-id="f9ed5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f9ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="f9ed5-103">Skapar ett IP-taggattribut för ett nätverks gränssnitt för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9ed5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f9ed5-104">SYNTAX</span></span>

```
New-AzureRmVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9ed5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f9ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="f9ed5-106">Cmdleten **New-AzureRmVmssIpTagConfig** skapar ett konfigurations objekt för IP-märkning för ett nätverks gränssnitt av en virtuell dators skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f9ed5-106">The **New-AzureRmVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f9ed5-107">Ange konfigurationen från denna cmdlet som *IPTag* -parameter för New-AzureRmVmssIpConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzureRmVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="f9ed5-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f9ed5-108">EXAMPLES</span></span>

### <span data-ttu-id="f9ed5-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f9ed5-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzureRmVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzureRmVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="f9ed5-110">Det här kommandot skapar ett lokalt IP-objekt med typen ' FirstPartyUsage ' och ' SQL '-märket och skapar sedan en IP-konfiguration med detta IP-märke.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="f9ed5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f9ed5-111">PARAMETERS</span></span>

### <span data-ttu-id="f9ed5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9ed5-112">-DefaultProfile</span></span>
<span data-ttu-id="f9ed5-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9ed5-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="f9ed5-114">-IpTagType</span></span>
<span data-ttu-id="f9ed5-115">Anger en IP-tagg.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="f9ed5-116">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f9ed5-116">-Tag</span></span>
<span data-ttu-id="f9ed5-117">Anger ett värde för IP-märkning.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="f9ed5-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f9ed5-118">-Confirm</span></span>
<span data-ttu-id="f9ed5-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ed5-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9ed5-120">-WhatIf</span></span>
<span data-ttu-id="f9ed5-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9ed5-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9ed5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9ed5-123">CommonParameters</span></span>
<span data-ttu-id="f9ed5-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9ed5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9ed5-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9ed5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9ed5-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f9ed5-126">INPUTS</span></span>

### <span data-ttu-id="f9ed5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f9ed5-127">System.String</span></span>

## <span data-ttu-id="f9ed5-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f9ed5-128">OUTPUTS</span></span>

### <span data-ttu-id="f9ed5-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="f9ed5-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="f9ed5-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f9ed5-130">NOTES</span></span>

## <span data-ttu-id="f9ed5-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f9ed5-131">RELATED LINKS</span></span>
