---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/install-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b9563e9b8b7afb7b980f0b3cd307c76fb9c6e8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575516"
---
# <span data-ttu-id="108a0-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="108a0-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="108a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="108a0-102">SYNOPSIS</span></span>
<span data-ttu-id="108a0-103">Installerar en Server Management Gateway-profil.</span><span class="sxs-lookup"><span data-stu-id="108a0-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="108a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="108a0-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="108a0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="108a0-105">DESCRIPTION</span></span>
<span data-ttu-id="108a0-106">Cmdleten **install-AzureRmServerManagementGatewayProfile** installerar en Azure Server Management Gateway-profil på rätt plats.</span><span class="sxs-lookup"><span data-stu-id="108a0-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="108a0-107">Filen som installeras med den här cmdleten kallas profile.jspå.</span><span class="sxs-lookup"><span data-stu-id="108a0-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="108a0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="108a0-108">EXAMPLES</span></span>

## <span data-ttu-id="108a0-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="108a0-109">PARAMETERS</span></span>

### <span data-ttu-id="108a0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="108a0-110">-DefaultProfile</span></span>
<span data-ttu-id="108a0-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="108a0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="108a0-112">-InputFile</span><span class="sxs-lookup"><span data-stu-id="108a0-112">-InputFile</span></span>
<span data-ttu-id="108a0-113">Anger namnet på den lokala filen som innehåller Gateway-profilen som ska installeras.</span><span class="sxs-lookup"><span data-stu-id="108a0-113">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="108a0-114">Filen som installeras av denna cmdlet bör tidigare ha sparats med Save-AzureRmServerManagementGatewayProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="108a0-114">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="108a0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="108a0-115">CommonParameters</span></span>
<span data-ttu-id="108a0-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="108a0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="108a0-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="108a0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="108a0-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="108a0-118">INPUTS</span></span>

### <span data-ttu-id="108a0-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="108a0-119">FileInfo</span></span>
<span data-ttu-id="108a0-120">Parametern ' InputFile ' godkänner värdet av typen ' FileInfo ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="108a0-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="108a0-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="108a0-121">OUTPUTS</span></span>

## <span data-ttu-id="108a0-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="108a0-122">NOTES</span></span>

## <span data-ttu-id="108a0-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="108a0-123">RELATED LINKS</span></span>

[<span data-ttu-id="108a0-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="108a0-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="108a0-125">Spara – AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="108a0-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


