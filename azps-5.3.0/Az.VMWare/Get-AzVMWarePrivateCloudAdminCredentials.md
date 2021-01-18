---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522154"
---
# <span data-ttu-id="da913-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="da913-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="da913-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da913-102">SYNOPSIS</span></span>
<span data-ttu-id="da913-103">Ange administratörsautentiseringsuppgifter för det privata molnet</span><span class="sxs-lookup"><span data-stu-id="da913-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="da913-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da913-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="da913-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da913-105">DESCRIPTION</span></span>
<span data-ttu-id="da913-106">Ange administratörsautentiseringsuppgifter för det privata molnet</span><span class="sxs-lookup"><span data-stu-id="da913-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="da913-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da913-107">EXAMPLES</span></span>

### <span data-ttu-id="da913-108">Exempel 1: skaffa administratörs behörighet för privata moln</span><span class="sxs-lookup"><span data-stu-id="da913-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="da913-109">Skaffa administratörs behörighet för privata moln</span><span class="sxs-lookup"><span data-stu-id="da913-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="da913-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da913-110">PARAMETERS</span></span>

### <span data-ttu-id="da913-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da913-111">-DefaultProfile</span></span>
<span data-ttu-id="da913-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da913-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da913-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="da913-113">-PrivateCloudName</span></span>
<span data-ttu-id="da913-114">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="da913-114">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da913-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da913-115">-ResourceGroupName</span></span>
<span data-ttu-id="da913-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="da913-116">The name of the resource group.</span></span>
<span data-ttu-id="da913-117">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="da913-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da913-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="da913-118">-SubscriptionId</span></span>
<span data-ttu-id="da913-119">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="da913-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da913-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="da913-120">-Confirm</span></span>
<span data-ttu-id="da913-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="da913-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da913-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da913-122">-WhatIf</span></span>
<span data-ttu-id="da913-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="da913-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da913-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="da913-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da913-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da913-125">CommonParameters</span></span>
<span data-ttu-id="da913-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da913-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da913-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da913-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da913-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da913-128">INPUTS</span></span>

## <span data-ttu-id="da913-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da913-129">OUTPUTS</span></span>

### <span data-ttu-id="da913-130">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="da913-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="da913-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da913-131">NOTES</span></span>

<span data-ttu-id="da913-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="da913-132">ALIASES</span></span>

## <span data-ttu-id="da913-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da913-133">RELATED LINKS</span></span>

