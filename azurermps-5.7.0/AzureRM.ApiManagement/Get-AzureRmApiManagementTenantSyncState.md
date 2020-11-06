---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: 64e1d8ad070d4ce1c2f8129a73efd8730f26d1a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576652"
---
# <span data-ttu-id="bb475-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="bb475-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="bb475-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb475-102">SYNOPSIS</span></span>
<span data-ttu-id="bb475-103">Får statusen för den senaste synkroniseringen mellan konfigurations databasen och git-databasen.</span><span class="sxs-lookup"><span data-stu-id="bb475-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb475-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb475-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb475-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb475-105">DESCRIPTION</span></span>
<span data-ttu-id="bb475-106">Cmdleten **Get-AzureRmApiManagementTenantSyncState** får statusen för den senaste synkroniseringen mellan konfigurations databasen och git-databasen.</span><span class="sxs-lookup"><span data-stu-id="bb475-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="bb475-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb475-107">EXAMPLES</span></span>

### <span data-ttu-id="bb475-108">Exempel 1: få statusen för den senaste synkroniseringen</span><span class="sxs-lookup"><span data-stu-id="bb475-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext 
```

<span data-ttu-id="bb475-109">Det här kommandot får statusen för den senaste synkroniseringen mellan konfigurations databasen och git-databasen.</span><span class="sxs-lookup"><span data-stu-id="bb475-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="bb475-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb475-110">PARAMETERS</span></span>

### <span data-ttu-id="bb475-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bb475-111">-Context</span></span>
<span data-ttu-id="bb475-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="bb475-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb475-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb475-113">-DefaultProfile</span></span>
<span data-ttu-id="bb475-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb475-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="bb475-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb475-115">CommonParameters</span></span>
<span data-ttu-id="bb475-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb475-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb475-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb475-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb475-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb475-118">INPUTS</span></span>

### <span data-ttu-id="bb475-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="bb475-119">None</span></span>
<span data-ttu-id="bb475-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="bb475-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bb475-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb475-121">OUTPUTS</span></span>

### <span data-ttu-id="bb475-122">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="bb475-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="bb475-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb475-123">NOTES</span></span>

## <span data-ttu-id="bb475-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb475-124">RELATED LINKS</span></span>

