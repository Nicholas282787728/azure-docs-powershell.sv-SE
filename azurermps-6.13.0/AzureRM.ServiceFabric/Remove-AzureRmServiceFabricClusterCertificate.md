---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 088f90af1ce80bdda390de1ce62a9d38581344aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576757"
---
# <span data-ttu-id="67e81-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="67e81-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="67e81-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="67e81-102">SYNOPSIS</span></span>
<span data-ttu-id="67e81-103">Ta bort ett kluster certifikat från att användas för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="67e81-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e81-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="67e81-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67e81-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="67e81-105">DESCRIPTION</span></span>
<span data-ttu-id="67e81-106">Använd **Remove-AzureRmServiceFabricClusterCertificate** för att ta bort ett kluster certifikat från klustret, förutsatt att det finns ett annat giltigt certifikat som redan används i klustret.</span><span class="sxs-lookup"><span data-stu-id="67e81-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="67e81-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="67e81-107">EXAMPLES</span></span>

### <span data-ttu-id="67e81-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="67e81-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="67e81-109">Det här kommandot tar bort certifikatet med tumavtrycket 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A som används för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="67e81-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="67e81-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="67e81-110">PARAMETERS</span></span>

### <span data-ttu-id="67e81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e81-111">-DefaultProfile</span></span>
<span data-ttu-id="67e81-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="67e81-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67e81-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="67e81-113">-Name</span></span>
<span data-ttu-id="67e81-114">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="67e81-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="67e81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e81-115">-ResourceGroupName</span></span>
<span data-ttu-id="67e81-116">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="67e81-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="67e81-117">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="67e81-117">-Thumbprint</span></span>
<span data-ttu-id="67e81-118">Ange det kluster-tumavtryck som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="67e81-118">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="67e81-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="67e81-119">-Confirm</span></span>
<span data-ttu-id="67e81-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="67e81-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e81-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e81-121">-WhatIf</span></span>
<span data-ttu-id="67e81-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="67e81-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67e81-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="67e81-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e81-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e81-124">CommonParameters</span></span>
<span data-ttu-id="67e81-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67e81-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e81-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e81-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e81-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="67e81-127">INPUTS</span></span>

### <span data-ttu-id="67e81-128">System. String</span><span class="sxs-lookup"><span data-stu-id="67e81-128">System.String</span></span>
<span data-ttu-id="67e81-129">Parametrar: tumavtryck (ByValue)</span><span class="sxs-lookup"><span data-stu-id="67e81-129">Parameters: Thumbprint (ByValue)</span></span>

## <span data-ttu-id="67e81-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="67e81-130">OUTPUTS</span></span>

### <span data-ttu-id="67e81-131">Microsoft. Azure. commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="67e81-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="67e81-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="67e81-132">NOTES</span></span>

## <span data-ttu-id="67e81-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="67e81-133">RELATED LINKS</span></span>
