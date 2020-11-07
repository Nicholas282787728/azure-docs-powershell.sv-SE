---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssiptagconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpTagConfig.md
ms.openlocfilehash: c6af342183b7f1b2aa9bf7695ba8486ec193698a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93928262"
---
# <span data-ttu-id="d44af-101">New-AzVmssIpTagConfig</span><span class="sxs-lookup"><span data-stu-id="d44af-101">New-AzVmssIpTagConfig</span></span>

## <span data-ttu-id="d44af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d44af-102">SYNOPSIS</span></span>
<span data-ttu-id="d44af-103">Skapar ett IP-taggattribut för ett nätverks gränssnitt för en VMSS.</span><span class="sxs-lookup"><span data-stu-id="d44af-103">Creates an IP Tag object for a network interface of a VMSS.</span></span>

## <span data-ttu-id="d44af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d44af-104">SYNTAX</span></span>

```
New-AzVmssIpTagConfig [-IpTagType] <String> [-Tag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d44af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d44af-105">DESCRIPTION</span></span>
<span data-ttu-id="d44af-106">Cmdleten **New-AzVmssIpTagConfig** skapar ett konfigurations objekt för IP-märkning för ett nätverks gränssnitt av en virtuell dators skal uppsättning (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d44af-106">The **New-AzVmssIpTagConfig** cmdlet creates an IP Tag configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="d44af-107">Ange konfigurationen från denna cmdlet som *IPTag* -parameter för New-AzVmssIpConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d44af-107">Specify the configuration from this cmdlet as the *IPTag* parameter of the New-AzVmssIpConfig cmdlet.</span></span>

## <span data-ttu-id="d44af-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d44af-108">EXAMPLES</span></span>

### <span data-ttu-id="d44af-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d44af-109">Example 1</span></span>
```powershell
PS C:\> $iptag = New-AzVmssIpTagConfig -IpTagType 'FirstPartyUsage' -Tag 'Sql'
PS C:\> $ipCfg = New-AzVmssIPConfig -Name 'test' -SubnetId $subnetId -IpTag $ipTag;
```

<span data-ttu-id="d44af-110">Det här kommandot skapar ett lokalt IP-objekt med typen ' FirstPartyUsage ' och ' SQL '-märket och skapar sedan en IP-konfiguration med detta IP-märke.</span><span class="sxs-lookup"><span data-stu-id="d44af-110">This command creates an IP Tag local object with 'FirstPartyUsage' type and 'Sql' tag, and then creates an IP configuration with this IP tag.</span></span>

## <span data-ttu-id="d44af-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d44af-111">PARAMETERS</span></span>

### <span data-ttu-id="d44af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d44af-112">-DefaultProfile</span></span>
<span data-ttu-id="d44af-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d44af-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d44af-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="d44af-114">-IpTagType</span></span>
<span data-ttu-id="d44af-115">Anger en IP-tagg.</span><span class="sxs-lookup"><span data-stu-id="d44af-115">Specifies an IP Tag Type.</span></span>

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

### <span data-ttu-id="d44af-116">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d44af-116">-Tag</span></span>
<span data-ttu-id="d44af-117">Anger ett värde för IP-märkning.</span><span class="sxs-lookup"><span data-stu-id="d44af-117">Specifies an IP Tag Value.</span></span>

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

### <span data-ttu-id="d44af-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d44af-118">-Confirm</span></span>
<span data-ttu-id="d44af-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d44af-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d44af-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d44af-120">-WhatIf</span></span>
<span data-ttu-id="d44af-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d44af-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d44af-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d44af-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d44af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d44af-123">CommonParameters</span></span>
<span data-ttu-id="d44af-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d44af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d44af-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d44af-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d44af-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d44af-126">INPUTS</span></span>

### <span data-ttu-id="d44af-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d44af-127">System.String</span></span>

## <span data-ttu-id="d44af-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d44af-128">OUTPUTS</span></span>

### <span data-ttu-id="d44af-129">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag</span><span class="sxs-lookup"><span data-stu-id="d44af-129">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag</span></span>

## <span data-ttu-id="d44af-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d44af-130">NOTES</span></span>

## <span data-ttu-id="d44af-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d44af-131">RELATED LINKS</span></span>
