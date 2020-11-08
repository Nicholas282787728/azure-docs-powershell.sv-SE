---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: d1a6859638bfbcb69e479f4bc18a6a36c8aa68fe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271830"
---
# <span data-ttu-id="6d00c-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6d00c-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="6d00c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d00c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d00c-103">Hämtar de protokollförda kategorierna och tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="6d00c-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="6d00c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d00c-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d00c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d00c-105">DESCRIPTION</span></span>
<span data-ttu-id="6d00c-106">Cmdleten **Get-AzDiagnosticSetting** hämtar kategorier och tidsintervall som är loggförda för en resurs.</span><span class="sxs-lookup"><span data-stu-id="6d00c-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="6d00c-107">En tids kornig het är agg regerings intervallet för ett mått.</span><span class="sxs-lookup"><span data-stu-id="6d00c-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="6d00c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d00c-108">EXAMPLES</span></span>

### <span data-ttu-id="6d00c-109">Exempel 1: få status för loggnings kategorier och tids kornig het</span><span class="sxs-lookup"><span data-stu-id="6d00c-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="6d00c-110">Det här kommandot får kategorier och tidsintervall som är loggförda för ett Azure Key-valv med *ResourceID* för/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6d00c-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="6d00c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d00c-111">PARAMETERS</span></span>

### <span data-ttu-id="6d00c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d00c-112">-DefaultProfile</span></span>
<span data-ttu-id="6d00c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6d00c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d00c-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d00c-114">-Name</span></span>
<span data-ttu-id="6d00c-115">Namnet på diagnos inställningen.</span><span class="sxs-lookup"><span data-stu-id="6d00c-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="6d00c-116">Om du inte har fått värdet "tjänst" som standard till det förra API: t.</span><span class="sxs-lookup"><span data-stu-id="6d00c-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="6d00c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d00c-117">-ResourceId</span></span>
<span data-ttu-id="6d00c-118">Anger ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="6d00c-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="6d00c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d00c-119">CommonParameters</span></span>
<span data-ttu-id="6d00c-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d00c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d00c-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d00c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d00c-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d00c-122">INPUTS</span></span>

### <span data-ttu-id="6d00c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6d00c-123">System.String</span></span>

## <span data-ttu-id="6d00c-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d00c-124">OUTPUTS</span></span>

### <span data-ttu-id="6d00c-125">Microsoft. Azure. commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="6d00c-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="6d00c-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d00c-126">NOTES</span></span>

## <span data-ttu-id="6d00c-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d00c-127">RELATED LINKS</span></span>

<span data-ttu-id="6d00c-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="6d00c-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
