---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvancedDataSecurityPolicy.md
ms.openlocfilehash: 9776f4a569c2b8ac47d3bc8e478ce9fbfaccab01
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261643"
---
# <span data-ttu-id="a6777-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="a6777-101">Get-AzSqlServerAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="a6777-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6777-102">SYNOPSIS</span></span>
<span data-ttu-id="a6777-103">Hämtar avancerade data säkerhets principer för en server.</span><span class="sxs-lookup"><span data-stu-id="a6777-103">Gets Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="a6777-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6777-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvancedDataSecurityPolicy [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6777-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6777-105">DESCRIPTION</span></span>
<span data-ttu-id="a6777-106">Cmdleten **Get-AzSqlServerAdvancedDataSecurityPolicy** hämtar den avancerade data säkerhets principen för en server.</span><span class="sxs-lookup"><span data-stu-id="a6777-106">The **Get-AzSqlServerAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a server.</span></span>

## <span data-ttu-id="a6777-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6777-107">EXAMPLES</span></span>

### <span data-ttu-id="a6777-108">Exempel 1: hämtar avancerad data säkerhet för servrar</span><span class="sxs-lookup"><span data-stu-id="a6777-108">Example 1: Gets server Advanced Data Security</span></span>
```powershell
PS C:\>  Get-AzSqlServerAdvancedDataSecurityPolicy `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

### <span data-ttu-id="a6777-109">Exempel 2: hämtar avancerad data säkerhet för servrar från Server resursen</span><span class="sxs-lookup"><span data-stu-id="a6777-109">Example 2: Gets server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Get-AzSqlServerAdvancedDataSecurityPolicy

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : True
```

## <span data-ttu-id="a6777-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6777-110">PARAMETERS</span></span>

### <span data-ttu-id="a6777-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6777-111">-DefaultProfile</span></span>
<span data-ttu-id="a6777-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6777-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6777-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6777-113">-InputObject</span></span>
<span data-ttu-id="a6777-114">Serverobjektet som ska användas med avancerad data säkerhets policy åtgärd</span><span class="sxs-lookup"><span data-stu-id="a6777-114">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="a6777-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6777-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6777-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a6777-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6777-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a6777-117">-ServerName</span></span>
<span data-ttu-id="a6777-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="a6777-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="a6777-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6777-119">CommonParameters</span></span>
<span data-ttu-id="a6777-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6777-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6777-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6777-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6777-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6777-122">INPUTS</span></span>

### <span data-ttu-id="a6777-123">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a6777-123">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="a6777-124">System. String</span><span class="sxs-lookup"><span data-stu-id="a6777-124">System.String</span></span>

## <span data-ttu-id="a6777-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6777-125">OUTPUTS</span></span>

### <span data-ttu-id="a6777-126">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a6777-126">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="a6777-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6777-127">NOTES</span></span>

## <span data-ttu-id="a6777-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6777-128">RELATED LINKS</span></span>
