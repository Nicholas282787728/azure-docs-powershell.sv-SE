---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 11CE6244-D287-4B99-9585-E3EA2D36A4F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 44addca6ee4f658f4cc6f8081e0f7a0c39ba4a58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581271"
---
# <span data-ttu-id="d6bbf-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d6bbf-101">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="d6bbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="d6bbf-103">Skapar en mappning för en Azure Site Recovery-behållare genom att associera en princip till en skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-103">Creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6bbf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6bbf-104">SYNTAX</span></span>

### <span data-ttu-id="d6bbf-105">EnterpriseToAzure (standard)</span><span class="sxs-lookup"><span data-stu-id="d6bbf-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6bbf-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="d6bbf-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryProtectionContainerMapping -Name <String> -Policy <ASRPolicy>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6bbf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6bbf-107">DESCRIPTION</span></span>
<span data-ttu-id="d6bbf-108">Cmdleten **New-AzureRmSiteRecoveryProtectionContainerMapping** skapar en Azure Site Recovery-mappning för att associera en princip till en skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-108">The **New-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet creates an Azure Site Recovery Protection Container mapping by associating a policy to a Protection Container.</span></span>

## <span data-ttu-id="d6bbf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6bbf-109">EXAMPLES</span></span>

## <span data-ttu-id="d6bbf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6bbf-110">PARAMETERS</span></span>

### <span data-ttu-id="d6bbf-111">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6bbf-111">-Name</span></span>
<span data-ttu-id="d6bbf-112">Anger namnet på skydds behållar mappningen.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-112">Specifies the name of the Protection Container mapping.</span></span>

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

### <span data-ttu-id="d6bbf-113">-Princip</span><span class="sxs-lookup"><span data-stu-id="d6bbf-113">-Policy</span></span>
<span data-ttu-id="d6bbf-114">Anger Azure Site Recovery policy-objekt.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-114">Specifies the Azure Site Recovery Policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6bbf-115">-PrimaryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d6bbf-115">-PrimaryProtectionContainer</span></span>
<span data-ttu-id="d6bbf-116">Anger primärt skydd behållar objekt.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-116">Specifies the primary Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bbf-117">-RecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d6bbf-117">-RecoveryProtectionContainer</span></span>
<span data-ttu-id="d6bbf-118">Anger återställnings skydds objekt.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-118">Specifies the Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6bbf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6bbf-119">-DefaultProfile</span></span>
<span data-ttu-id="d6bbf-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6bbf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6bbf-121">CommonParameters</span></span>
<span data-ttu-id="d6bbf-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6bbf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6bbf-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6bbf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6bbf-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6bbf-124">INPUTS</span></span>

### <span data-ttu-id="d6bbf-125">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="d6bbf-125">ASRPolicy</span></span>
<span data-ttu-id="d6bbf-126">Parametern ' policy ' godkänner värdet av typen ' ASRPolicy ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d6bbf-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="d6bbf-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6bbf-127">OUTPUTS</span></span>

### <span data-ttu-id="d6bbf-128">Microsoft. Azure. commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d6bbf-128">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d6bbf-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6bbf-129">NOTES</span></span>

## <span data-ttu-id="d6bbf-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6bbf-130">RELATED LINKS</span></span>

[<span data-ttu-id="d6bbf-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d6bbf-131">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="d6bbf-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d6bbf-132">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Remove-AzureRmSiteRecoveryProtectionContainerMapping.md)
