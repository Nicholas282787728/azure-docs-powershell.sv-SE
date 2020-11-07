---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlserveradvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlServerAdvancedDataSecurity.md
ms.openlocfilehash: 482a620552457993795ba03e2da9367df5efa614
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925530"
---
# <span data-ttu-id="a8293-101">Disable-AzSqlServerAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="a8293-101">Disable-AzSqlServerAdvancedDataSecurity</span></span>

## <span data-ttu-id="a8293-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8293-102">SYNOPSIS</span></span>
<span data-ttu-id="a8293-103">Inaktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="a8293-103">Disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="a8293-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8293-104">SYNTAX</span></span>

```
Disable-AzSqlServerAdvancedDataSecurity [-InputObject <AzureSqlServerModel>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8293-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8293-105">DESCRIPTION</span></span>
<span data-ttu-id="a8293-106">Cmdleten **disable-AzSqlServerAdvancedDataSecurity** inaktiverar avancerad data säkerhet på en server.</span><span class="sxs-lookup"><span data-stu-id="a8293-106">The **Disable-AzSqlServerAdvancedDataSecurity** cmdlet disables Advanced Data Security on a server.</span></span>

## <span data-ttu-id="a8293-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8293-107">EXAMPLES</span></span>

### <span data-ttu-id="a8293-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8293-108">Example 1</span></span>
### <span data-ttu-id="a8293-109">Exempel 1 – inaktivera avancerad data säkerhet för servrar</span><span class="sxs-lookup"><span data-stu-id="a8293-109">Example 1 - Disable server Advanced Data Security</span></span>
```powershell
PS C:\>  Disable-AzSqlServerAdvancedDataSecurity `
            -ResourceGroupName "ResourceGroup01" `
            -ServerName "Server01" 

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

### <span data-ttu-id="a8293-110">Exempel 2 – inaktivera avancerad data säkerhet för servrar från Server resurs</span><span class="sxs-lookup"><span data-stu-id="a8293-110">Example 2 - Disable server Advanced Data Security from server resource</span></span>
```powershell
PS C:\>  Get-AzSqlServer `
           -ResourceGroupName "ResourceGroup01" `
           -ServerName "Server01" `
           | Disable-AzSqlServerAdvancedDataSecurity

ResourceGroupName            : ResourceGroup01
ServerName                   : Server01
IsEnabled                    : False
```

## <span data-ttu-id="a8293-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8293-111">PARAMETERS</span></span>

### <span data-ttu-id="a8293-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8293-112">-DefaultProfile</span></span>
<span data-ttu-id="a8293-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8293-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8293-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8293-114">-InputObject</span></span>
<span data-ttu-id="a8293-115">Serverobjektet som ska användas med avancerad data säkerhets policy åtgärd</span><span class="sxs-lookup"><span data-stu-id="a8293-115">The server object to use with Advanced Data Security policy operation</span></span>

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

### <span data-ttu-id="a8293-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8293-116">-ResourceGroupName</span></span>
<span data-ttu-id="a8293-117">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a8293-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8293-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a8293-118">-ServerName</span></span>
<span data-ttu-id="a8293-119">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="a8293-119">SQL Database server name.</span></span>

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

### <span data-ttu-id="a8293-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8293-120">-Confirm</span></span>
<span data-ttu-id="a8293-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8293-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8293-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8293-122">-WhatIf</span></span>
<span data-ttu-id="a8293-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8293-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8293-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8293-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8293-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8293-125">CommonParameters</span></span>
<span data-ttu-id="a8293-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8293-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8293-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8293-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8293-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8293-128">INPUTS</span></span>

### <span data-ttu-id="a8293-129">Microsoft. Azure. commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="a8293-129">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="a8293-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a8293-130">System.String</span></span>

## <span data-ttu-id="a8293-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8293-131">OUTPUTS</span></span>

### <span data-ttu-id="a8293-132">Microsoft. Azure. commands. SQL. AdvancedThreatProtection. Model. ServerAdvancedDataSecurityPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a8293-132">Microsoft.Azure.Commands.Sql.AdvancedThreatProtection.Model.ServerAdvancedDataSecurityPolicyModel</span></span>

## <span data-ttu-id="a8293-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8293-133">NOTES</span></span>

## <span data-ttu-id="a8293-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8293-134">RELATED LINKS</span></span>
