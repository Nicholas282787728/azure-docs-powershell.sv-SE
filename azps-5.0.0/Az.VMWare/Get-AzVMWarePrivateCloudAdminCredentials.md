---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271668"
---
# <span data-ttu-id="1b2f0-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="1b2f0-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="1b2f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b2f0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2f0-103">Ange administratörsautentiseringsuppgifter för det privata molnet</span><span class="sxs-lookup"><span data-stu-id="1b2f0-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="1b2f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b2f0-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b2f0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b2f0-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2f0-106">Ange administratörsautentiseringsuppgifter för det privata molnet</span><span class="sxs-lookup"><span data-stu-id="1b2f0-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="1b2f0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b2f0-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2f0-108">Exempel 1: skaffa administratörs behörighet för privata moln</span><span class="sxs-lookup"><span data-stu-id="1b2f0-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="1b2f0-109">Skaffa administratörs behörighet för privata moln</span><span class="sxs-lookup"><span data-stu-id="1b2f0-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="1b2f0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b2f0-110">PARAMETERS</span></span>

### <span data-ttu-id="1b2f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2f0-111">-DefaultProfile</span></span>
<span data-ttu-id="1b2f0-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b2f0-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="1b2f0-113">-PrivateCloudName</span></span>
<span data-ttu-id="1b2f0-114">Namn på det privata molnet</span><span class="sxs-lookup"><span data-stu-id="1b2f0-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="1b2f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="1b2f0-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-116">The name of the resource group.</span></span>
<span data-ttu-id="1b2f0-117">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="1b2f0-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b2f0-118">-SubscriptionId</span></span>
<span data-ttu-id="1b2f0-119">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="1b2f0-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b2f0-120">-Confirm</span></span>
<span data-ttu-id="1b2f0-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b2f0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2f0-122">-WhatIf</span></span>
<span data-ttu-id="1b2f0-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2f0-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b2f0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2f0-125">CommonParameters</span></span>
<span data-ttu-id="1b2f0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b2f0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2f0-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b2f0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2f0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b2f0-128">INPUTS</span></span>

## <span data-ttu-id="1b2f0-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b2f0-129">OUTPUTS</span></span>

### <span data-ttu-id="1b2f0-130">Microsoft. Azure. PowerShell. cmdletar. VMWare. Models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="1b2f0-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="1b2f0-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b2f0-131">NOTES</span></span>

<span data-ttu-id="1b2f0-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1b2f0-132">ALIASES</span></span>

## <span data-ttu-id="1b2f0-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b2f0-133">RELATED LINKS</span></span>
