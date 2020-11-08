---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantSyncState.md
ms.openlocfilehash: 233c74e3939884cd4bd311ec463d81d7e7613f31
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090579"
---
# <span data-ttu-id="d1c5b-101">Get-AzApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="d1c5b-101">Get-AzApiManagementTenantSyncState</span></span>

## <span data-ttu-id="d1c5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1c5b-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c5b-103">Får statusen för den senaste synkroniseringen mellan konfigurations databasen och git-databasen.</span><span class="sxs-lookup"><span data-stu-id="d1c5b-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="d1c5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1c5b-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantSyncState -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1c5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1c5b-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c5b-106">Cmdleten **Get-AzApiManagementTenantSyncState** får statusen för den senaste synkroniseringen mellan konfigurations databasen och git-databasen.</span><span class="sxs-lookup"><span data-stu-id="d1c5b-106">The **Get-AzApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="d1c5b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1c5b-107">EXAMPLES</span></span>

### <span data-ttu-id="d1c5b-108">Exempel 1: få statusen för den senaste synkroniseringen</span><span class="sxs-lookup"><span data-stu-id="d1c5b-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantSyncState -Context $apimContext
```

<span data-ttu-id="d1c5b-109">Det här kommandot får statusen för den senaste synkroniseringen mellan konfigurations databasen och git-databasen.</span><span class="sxs-lookup"><span data-stu-id="d1c5b-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="d1c5b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1c5b-110">PARAMETERS</span></span>

### <span data-ttu-id="d1c5b-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d1c5b-111">-Context</span></span>
<span data-ttu-id="d1c5b-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d1c5b-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1c5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c5b-113">-DefaultProfile</span></span>
<span data-ttu-id="d1c5b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1c5b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1c5b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c5b-115">CommonParameters</span></span>
<span data-ttu-id="d1c5b-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c5b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c5b-117">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1c5b-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c5b-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1c5b-118">INPUTS</span></span>

### <span data-ttu-id="d1c5b-119">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1c5b-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="d1c5b-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1c5b-120">OUTPUTS</span></span>

### <span data-ttu-id="d1c5b-121">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementTenantConfigurationSyncState</span><span class="sxs-lookup"><span data-stu-id="d1c5b-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementTenantConfigurationSyncState</span></span>

## <span data-ttu-id="d1c5b-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1c5b-122">NOTES</span></span>

## <span data-ttu-id="d1c5b-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1c5b-123">RELATED LINKS</span></span>