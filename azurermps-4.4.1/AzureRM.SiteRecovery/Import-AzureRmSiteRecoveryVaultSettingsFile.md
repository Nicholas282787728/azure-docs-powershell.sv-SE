---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584516"
---
# <span data-ttu-id="ff311-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ff311-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="ff311-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff311-102">SYNOPSIS</span></span>
<span data-ttu-id="ff311-103">Importerar en inställnings fil för en webbplats återställnings valv.</span><span class="sxs-lookup"><span data-stu-id="ff311-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff311-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff311-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff311-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff311-105">DESCRIPTION</span></span>
<span data-ttu-id="ff311-106">Cmdleten **import-AzureRmSiteRecoveryVaultSettingsFile** importerar en Azure Site Recovery-inställnings fil för att ange valv kontexten för efterföljande webbplats återställnings åtgärder i den aktuella sessionen.</span><span class="sxs-lookup"><span data-stu-id="ff311-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="ff311-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff311-107">EXAMPLES</span></span>

## <span data-ttu-id="ff311-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff311-108">PARAMETERS</span></span>

### <span data-ttu-id="ff311-109">-Path</span><span class="sxs-lookup"><span data-stu-id="ff311-109">-Path</span></span>
<span data-ttu-id="ff311-110">Anger sökvägen till filen inställningar för valv för webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="ff311-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="ff311-111">Den här filen kan hämtas från portalen för webbplats återställnings valv och lagras lokalt.</span><span class="sxs-lookup"><span data-stu-id="ff311-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="ff311-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff311-112">-DefaultProfile</span></span>
<span data-ttu-id="ff311-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff311-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff311-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff311-114">CommonParameters</span></span>
<span data-ttu-id="ff311-115">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff311-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff311-116">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff311-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff311-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff311-117">INPUTS</span></span>

## <span data-ttu-id="ff311-118">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff311-118">OUTPUTS</span></span>

### <span data-ttu-id="ff311-119">Microsoft. Azure. commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="ff311-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="ff311-120">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff311-120">NOTES</span></span>

## <span data-ttu-id="ff311-121">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff311-121">RELATED LINKS</span></span>

[<span data-ttu-id="ff311-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ff311-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
