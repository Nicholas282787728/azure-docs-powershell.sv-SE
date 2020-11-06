---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: 16762b56995b90422c78ad6dc5dd87461c0a8317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579939"
---
# <span data-ttu-id="0606a-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0606a-101">Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="0606a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0606a-102">SYNOPSIS</span></span>
<span data-ttu-id="0606a-103">Hämtar en servers avancerade skydds policy.</span><span class="sxs-lookup"><span data-stu-id="0606a-103">Gets Advanced Threat Protection policy of a server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0606a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0606a-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0606a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0606a-105">DESCRIPTION</span></span>
<span data-ttu-id="0606a-106">Cmdleten **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** för att skydda en server.</span><span class="sxs-lookup"><span data-stu-id="0606a-106">The **Get-AzureRmSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="0606a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0606a-107">EXAMPLES</span></span>

### <span data-ttu-id="0606a-108">Exempel 1 – får Avancerat skydd mot Server</span><span class="sxs-lookup"><span data-stu-id="0606a-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="0606a-109">Exempel 2 – får Avancerat skydd mot Server resurs</span><span class="sxs-lookup"><span data-stu-id="0606a-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzureRmSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzureRmSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="0606a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0606a-110">PARAMETERS</span></span>

### <span data-ttu-id="0606a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0606a-111">-DefaultProfile</span></span>
<span data-ttu-id="0606a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0606a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0606a-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0606a-113">-InputObject</span></span>
<span data-ttu-id="0606a-114">Serverobjektet som ska användas med åtgärden för avancerad skydds policy</span><span class="sxs-lookup"><span data-stu-id="0606a-114">The server object to use with Advanced Threat Protection policy operation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0606a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0606a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0606a-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="0606a-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="0606a-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0606a-117">-ServerName</span></span>
<span data-ttu-id="0606a-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="0606a-118">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0606a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0606a-119">CommonParameters</span></span>
<span data-ttu-id="0606a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0606a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0606a-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0606a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0606a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0606a-122">INPUTS</span></span>

### <span data-ttu-id="0606a-123">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="0606a-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>
<span data-ttu-id="0606a-124">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0606a-124">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0606a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0606a-125">System.String</span></span>

## <span data-ttu-id="0606a-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0606a-126">OUTPUTS</span></span>

### <span data-ttu-id="0606a-127">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0606a-127">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="0606a-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0606a-128">NOTES</span></span>

## <span data-ttu-id="0606a-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0606a-129">RELATED LINKS</span></span>
