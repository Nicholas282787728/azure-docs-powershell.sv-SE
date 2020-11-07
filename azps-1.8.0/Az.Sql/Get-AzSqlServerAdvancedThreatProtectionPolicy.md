---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvancedthreatprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedThreatProtectionPolicy.md
ms.openlocfilehash: dce8018e97e01c10356e77d321d564690cc03f71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746682"
---
# <span data-ttu-id="3ecd7-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3ecd7-101">Get-AzSqlServerAdvancedThreatProtectionPolicy</span></span>

## <span data-ttu-id="3ecd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ecd7-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecd7-103">Hämtar en servers avancerade skydds policy.</span><span class="sxs-lookup"><span data-stu-id="3ecd7-103">Gets Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="3ecd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ecd7-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedThreatProtectionPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ecd7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ecd7-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecd7-106">Cmdleten **Get-AzSqlServerAdvancedThreatProtectionPolicy** för att skydda en server.</span><span class="sxs-lookup"><span data-stu-id="3ecd7-106">The **Get-AzSqlServerAdvancedThreatProtectionPolicy** cmdlet retrives the Advanced Threat Protection policy of a server.</span></span>

## <span data-ttu-id="3ecd7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ecd7-107">EXAMPLES</span></span>

### <span data-ttu-id="3ecd7-108">Exempel 1 – får Avancerat skydd mot Server</span><span class="sxs-lookup"><span data-stu-id="3ecd7-108">Example 1 - Gets server Advanced Threat Protection</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedThreatProtectionPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="3ecd7-109">Exempel 2 – får Avancerat skydd mot Server resurs</span><span class="sxs-lookup"><span data-stu-id="3ecd7-109">Example 2 - Gets server Advanced Threat Protection from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedThreatProtectionPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="3ecd7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ecd7-110">PARAMETERS</span></span>

### <span data-ttu-id="3ecd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecd7-111">-DefaultProfile</span></span>
<span data-ttu-id="3ecd7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ecd7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ecd7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ecd7-113">-InputObject</span></span>
<span data-ttu-id="3ecd7-114">Serverobjektet som ska användas med åtgärden för avancerad skydds policy</span><span class="sxs-lookup"><span data-stu-id="3ecd7-114">The server object to use with Advanced Threat Protection policy operation</span></span>

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

### <span data-ttu-id="3ecd7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ecd7-115">-ResourceGroupName</span></span>
<span data-ttu-id="3ecd7-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3ecd7-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="3ecd7-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ecd7-117">-ServerName</span></span>
<span data-ttu-id="3ecd7-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="3ecd7-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="3ecd7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecd7-119">CommonParameters</span></span>
<span data-ttu-id="3ecd7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ecd7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecd7-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ecd7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecd7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ecd7-122">INPUTS</span></span>

### <span data-ttu-id="3ecd7-123">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="3ecd7-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="3ecd7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3ecd7-124">System.String</span></span>

## <span data-ttu-id="3ecd7-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ecd7-125">OUTPUTS</span></span>

### <span data-ttu-id="3ecd7-126">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedThreatProtectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3ecd7-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedThreatProtectionPolicyModel</span></span>

## <span data-ttu-id="3ecd7-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ecd7-127">NOTES</span></span>

## <span data-ttu-id="3ecd7-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ecd7-128">RELATED LINKS</span></span>
