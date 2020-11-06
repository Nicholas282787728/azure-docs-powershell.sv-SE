---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 0ef59a8071438fa1bfd1560ab2f2102722aa335f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575829"
---
# <span data-ttu-id="eb2d5-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="eb2d5-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="eb2d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb2d5-103">Ta bort ett kluster certifikat från att användas för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb2d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb2d5-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb2d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb2d5-105">DESCRIPTION</span></span>
<span data-ttu-id="eb2d5-106">Använd **Remove-AzureRmServiceFabricClusterCertificate** för att ta bort ett kluster certifikat från klustret, förutsatt att det finns ett annat giltigt certifikat som redan används i klustret.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="eb2d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb2d5-107">EXAMPLES</span></span>

### <span data-ttu-id="eb2d5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="eb2d5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="eb2d5-109">Det här kommandot tar bort certifikatet med tumavtrycket 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A som används för kluster säkerhet.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="eb2d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb2d5-110">PARAMETERS</span></span>

### <span data-ttu-id="eb2d5-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb2d5-111">-Name</span></span>
<span data-ttu-id="eb2d5-112">Ange namnet på klustret.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="eb2d5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb2d5-113">-ResourceGroupName</span></span>
<span data-ttu-id="eb2d5-114">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eb2d5-115">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="eb2d5-115">-Thumbprint</span></span>
<span data-ttu-id="eb2d5-116">Ange det kluster-tumavtryck som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-116">Specify the cluster thumbprint which to be removed.</span></span>

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

### <span data-ttu-id="eb2d5-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb2d5-117">-Confirm</span></span>
<span data-ttu-id="eb2d5-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb2d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb2d5-119">-WhatIf</span></span>
<span data-ttu-id="eb2d5-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb2d5-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb2d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb2d5-122">-DefaultProfile</span></span>
<span data-ttu-id="eb2d5-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb2d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb2d5-124">CommonParameters</span></span>
<span data-ttu-id="eb2d5-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb2d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb2d5-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb2d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb2d5-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb2d5-127">INPUTS</span></span>

### <span data-ttu-id="eb2d5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb2d5-128">System.String</span></span>

## <span data-ttu-id="eb2d5-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb2d5-129">OUTPUTS</span></span>

### <span data-ttu-id="eb2d5-130">Microsoft. Azure. commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="eb2d5-130">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="eb2d5-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb2d5-131">NOTES</span></span>

## <span data-ttu-id="eb2d5-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb2d5-132">RELATED LINKS</span></span>

