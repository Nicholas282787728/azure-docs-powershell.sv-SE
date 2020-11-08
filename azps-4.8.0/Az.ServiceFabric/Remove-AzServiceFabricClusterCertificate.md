---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261682"
---
# <span data-ttu-id="5d734-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="5d734-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="5d734-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d734-102">SYNOPSIS</span></span>
<span data-ttu-id="5d734-103">Ta bort ett kluster certifikat från att användas för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="5d734-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="5d734-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d734-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d734-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d734-105">DESCRIPTION</span></span>
<span data-ttu-id="5d734-106">Använd **Remove-AzServiceFabricClusterCertificate** för att ta bort ett kluster certifikat från klustret, förutsatt att det finns ett annat giltigt certifikat som redan används i klustret.</span><span class="sxs-lookup"><span data-stu-id="5d734-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="5d734-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d734-107">EXAMPLES</span></span>

### <span data-ttu-id="5d734-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5d734-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="5d734-109">Det här kommandot tar bort certifikatet med tumavtrycket 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A som används för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="5d734-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="5d734-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d734-110">PARAMETERS</span></span>

### <span data-ttu-id="5d734-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d734-111">-DefaultProfile</span></span>
<span data-ttu-id="5d734-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d734-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d734-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d734-113">-Name</span></span>
<span data-ttu-id="5d734-114">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="5d734-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d734-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d734-115">-ResourceGroupName</span></span>
<span data-ttu-id="5d734-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5d734-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5d734-117">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="5d734-117">-Thumbprint</span></span>
<span data-ttu-id="5d734-118">Ange det kluster-tumavtryck som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="5d734-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d734-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d734-119">-Confirm</span></span>
<span data-ttu-id="5d734-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d734-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d734-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d734-121">-WhatIf</span></span>
<span data-ttu-id="5d734-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d734-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d734-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d734-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d734-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d734-124">CommonParameters</span></span>
<span data-ttu-id="5d734-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d734-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d734-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d734-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d734-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d734-127">INPUTS</span></span>

### <span data-ttu-id="5d734-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5d734-128">System.String</span></span>

## <span data-ttu-id="5d734-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d734-129">OUTPUTS</span></span>

### <span data-ttu-id="5d734-130">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="5d734-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5d734-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d734-131">NOTES</span></span>

## <span data-ttu-id="5d734-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d734-132">RELATED LINKS</span></span>
