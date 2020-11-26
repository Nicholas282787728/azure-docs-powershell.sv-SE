---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5ede0387f5aabb1a4f4c4814f8090e0feeda2bf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325056"
---
# <span data-ttu-id="4dd3a-101">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4dd3a-101">Get-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="4dd3a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4dd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd3a-103">Hämtar information om de ASR Recovery Services-leverantörer som registrerats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

## <span data-ttu-id="4dd3a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4dd3a-104">SYNTAX</span></span>

### <span data-ttu-id="4dd3a-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="4dd3a-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4dd3a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4dd3a-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4dd3a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4dd3a-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dd3a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4dd3a-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd3a-109">Cmdleten **Get-AzRecoveryServicesAsrServicesProvider** hämtar information om Azure Site Recovery-leverantörer i valvet.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-109">The **Get-AzRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="4dd3a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4dd3a-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd3a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4dd3a-111">Example 1</span></span>
```powershell
PS C:\> $RSPs = Get-AzRecoveryServicesAsrFabric | Get-AzRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="4dd3a-112">Lista alla ASR-leverantörer registrerade i det Recovery Services-valv som motsvarar den angivna Fabric-resursen.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

### <span data-ttu-id="4dd3a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4dd3a-113">Example 2</span></span>

<span data-ttu-id="4dd3a-114">Hämtar information om de ASR Recovery Services-leverantörer som registrerats för Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-114">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span> <span data-ttu-id="4dd3a-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="4dd3a-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrServicesProvider -Fabric $Fabric
```

## <span data-ttu-id="4dd3a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4dd3a-116">PARAMETERS</span></span>

### <span data-ttu-id="4dd3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd3a-117">-DefaultProfile</span></span>
<span data-ttu-id="4dd3a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4dd3a-119">-Fabric</span><span class="sxs-lookup"><span data-stu-id="4dd3a-119">-Fabric</span></span>
<span data-ttu-id="4dd3a-120">Anger ASR-Fabric-objekt.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-120">Specifies the ASR fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dd3a-121">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4dd3a-121">-FriendlyName</span></span>
<span data-ttu-id="4dd3a-122">Anger det egna namnet på ASR Recovery Services-leverantören för att få information om.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-122">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd3a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4dd3a-123">-Name</span></span>
<span data-ttu-id="4dd3a-124">Anger namnet på ASR Recovery Services-leverantören för att få information om.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-124">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dd3a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd3a-125">CommonParameters</span></span>
<span data-ttu-id="4dd3a-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd3a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd3a-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dd3a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd3a-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4dd3a-128">INPUTS</span></span>

### <span data-ttu-id="4dd3a-129">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4dd3a-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4dd3a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4dd3a-130">OUTPUTS</span></span>

### <span data-ttu-id="4dd3a-131">Microsoft. Azure. commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4dd3a-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="4dd3a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4dd3a-132">NOTES</span></span>

## <span data-ttu-id="4dd3a-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4dd3a-133">RELATED LINKS</span></span>

[<span data-ttu-id="4dd3a-134">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4dd3a-134">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="4dd3a-135">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4dd3a-135">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)