---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755920"
---
# <span data-ttu-id="72141-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="72141-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="72141-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72141-102">SYNOPSIS</span></span>
<span data-ttu-id="72141-103">Installerar en Server Management Gateway-profil.</span><span class="sxs-lookup"><span data-stu-id="72141-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72141-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72141-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72141-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72141-105">DESCRIPTION</span></span>
<span data-ttu-id="72141-106">Cmdleten **install-AzureRmServerManagementGatewayProfile** installerar en Azure Server Management Gateway-profil på rätt plats.</span><span class="sxs-lookup"><span data-stu-id="72141-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="72141-107">Filen som installeras med den här cmdleten kallas profile.jspå.</span><span class="sxs-lookup"><span data-stu-id="72141-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="72141-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72141-108">EXAMPLES</span></span>

## <span data-ttu-id="72141-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72141-109">PARAMETERS</span></span>

### <span data-ttu-id="72141-110">-InputFile</span><span class="sxs-lookup"><span data-stu-id="72141-110">-InputFile</span></span>
<span data-ttu-id="72141-111">Anger namnet på den lokala filen som innehåller Gateway-profilen som ska installeras.</span><span class="sxs-lookup"><span data-stu-id="72141-111">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="72141-112">Filen som installeras av denna cmdlet bör tidigare ha sparats med Save-AzureRmServerManagementGatewayProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72141-112">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72141-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72141-113">-DefaultProfile</span></span>
<span data-ttu-id="72141-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72141-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72141-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72141-115">CommonParameters</span></span>
<span data-ttu-id="72141-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72141-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72141-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72141-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72141-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72141-118">INPUTS</span></span>

### <span data-ttu-id="72141-119">FileInfo</span><span class="sxs-lookup"><span data-stu-id="72141-119">FileInfo</span></span>
<span data-ttu-id="72141-120">Parametern ' InputFile ' godkänner värdet av typen ' FileInfo ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="72141-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="72141-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72141-121">OUTPUTS</span></span>

## <span data-ttu-id="72141-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72141-122">NOTES</span></span>

## <span data-ttu-id="72141-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72141-123">RELATED LINKS</span></span>

[<span data-ttu-id="72141-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="72141-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="72141-125">Spara – AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="72141-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


