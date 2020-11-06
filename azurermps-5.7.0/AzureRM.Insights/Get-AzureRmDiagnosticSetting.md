---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: b5963aa588672bb2a8940d3f61f4cd67bef9c4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573426"
---
# <span data-ttu-id="9586d-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9586d-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="9586d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9586d-102">SYNOPSIS</span></span>
<span data-ttu-id="9586d-103">Hämtar de protokollförda kategorierna och tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="9586d-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9586d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9586d-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9586d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9586d-105">DESCRIPTION</span></span>
<span data-ttu-id="9586d-106">Cmdleten **Get-AzureRmDiagnosticSetting** hämtar kategorier och tidsintervall som är loggförda för en resurs.</span><span class="sxs-lookup"><span data-stu-id="9586d-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="9586d-107">En tids kornig het är agg regerings intervallet för ett mått.</span><span class="sxs-lookup"><span data-stu-id="9586d-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="9586d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9586d-108">EXAMPLES</span></span>

### <span data-ttu-id="9586d-109">Exempel 1: få status för loggnings kategorier och tids kornig het</span><span class="sxs-lookup"><span data-stu-id="9586d-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="9586d-110">Det här kommandot får kategorier och tidsintervall som är loggförda för ett Azure Key-valv med *ResourceID* för/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="9586d-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="9586d-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9586d-111">PARAMETERS</span></span>

### <span data-ttu-id="9586d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9586d-112">-DefaultProfile</span></span>
<span data-ttu-id="9586d-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9586d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9586d-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9586d-114">-ResourceId</span></span>
<span data-ttu-id="9586d-115">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="9586d-115">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9586d-116">CommonParameters</span></span>
<span data-ttu-id="9586d-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9586d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9586d-118">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9586d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9586d-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9586d-119">INPUTS</span></span>

### <span data-ttu-id="9586d-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="9586d-120">None</span></span>
<span data-ttu-id="9586d-121">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9586d-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9586d-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9586d-122">OUTPUTS</span></span>

### <span data-ttu-id="9586d-123">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="9586d-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="9586d-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9586d-124">NOTES</span></span>

## <span data-ttu-id="9586d-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9586d-125">RELATED LINKS</span></span>

[<span data-ttu-id="9586d-126">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="9586d-126">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


