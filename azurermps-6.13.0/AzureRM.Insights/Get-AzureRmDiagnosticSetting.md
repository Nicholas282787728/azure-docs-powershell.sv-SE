---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 2b70fd58bd0b51e03079b1c24665b67ac3ad3a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576988"
---
# <span data-ttu-id="aa1cb-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="aa1cb-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="aa1cb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa1cb-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1cb-103">Hämtar de protokollförda kategorierna och tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa1cb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa1cb-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa1cb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa1cb-105">DESCRIPTION</span></span>
<span data-ttu-id="aa1cb-106">Cmdleten **Get-AzureRmDiagnosticSetting** hämtar kategorier och tidsintervall som är loggförda för en resurs.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="aa1cb-107">En tids kornig het är agg regerings intervallet för ett mått.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="aa1cb-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa1cb-108">EXAMPLES</span></span>

### <span data-ttu-id="aa1cb-109">Exempel 1: få status för loggnings kategorier och tids kornig het</span><span class="sxs-lookup"><span data-stu-id="aa1cb-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="aa1cb-110">Det här kommandot får kategorier och tidsintervall som är loggförda för ett Azure Key-valv med *ResourceID* för/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="aa1cb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa1cb-111">PARAMETERS</span></span>

### <span data-ttu-id="aa1cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1cb-112">-DefaultProfile</span></span>
<span data-ttu-id="aa1cb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aa1cb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa1cb-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa1cb-114">-Name</span></span>
<span data-ttu-id="aa1cb-115">Namnet på diagnos inställningen.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="aa1cb-116">Om du inte har fått värdet "tjänst" som standard till det förra API: t.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-116">If not given the call default to "service" as it was in the previous API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa1cb-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa1cb-117">-ResourceId</span></span>
<span data-ttu-id="aa1cb-118">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="aa1cb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1cb-119">CommonParameters</span></span>
<span data-ttu-id="aa1cb-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa1cb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1cb-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa1cb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1cb-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa1cb-122">INPUTS</span></span>

### <span data-ttu-id="aa1cb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aa1cb-123">System.String</span></span>

## <span data-ttu-id="aa1cb-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa1cb-124">OUTPUTS</span></span>

### <span data-ttu-id="aa1cb-125">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="aa1cb-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="aa1cb-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa1cb-126">NOTES</span></span>

## <span data-ttu-id="aa1cb-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa1cb-127">RELATED LINKS</span></span>

<span data-ttu-id="aa1cb-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="aa1cb-128">[Set-AzureRmDiagnosticSetting](./Set-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
