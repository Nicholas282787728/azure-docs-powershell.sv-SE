---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryonlyauthentication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryOnlyAuthentication.md
ms.openlocfilehash: e5460fcbc48d36dab6309891247315f0539ff7ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269917"
---
# <span data-ttu-id="3cfa1-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3cfa1-101">Get-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>

## <span data-ttu-id="3cfa1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3cfa1-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfa1-103">Hämtar Azure AD-inloggningsautentisering för en viss SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-103">Gets Azure AD only authentication for a specific SQL Server.</span></span>

## <span data-ttu-id="3cfa1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3cfa1-104">SYNTAX</span></span>

### <span data-ttu-id="3cfa1-105">UseResourceGroupAndServerNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3cfa1-105">UseResourceGroupAndServerNameParameterSet (Default)</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceGroupName] <String> [-ServerName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfa1-106">UseInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cfa1-106">UseInputObjectParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication -InputObject <AzureSqlServerModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cfa1-107">UserResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cfa1-107">UserResourceIdParameterSet</span></span>
```
Get-AzSqlServerActiveDirectoryOnlyAuthentication [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cfa1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3cfa1-108">DESCRIPTION</span></span>
<span data-ttu-id="3cfa1-109">Cmdleten **Get-AzSqlServerActiveDirectoryOnlyAuthentication** får Azure Active Directory (Azure AD) autentiseringskrav endast för en AzureSQL-server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-109">The **Get-AzSqlServerActiveDirectoryOnlyAuthentication** cmdlet gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="3cfa1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3cfa1-110">EXAMPLES</span></span>

### <span data-ttu-id="3cfa1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3cfa1-111">Example 1</span></span>
```powershell
PS C:\>Get-AzSqlServerActiveDirectoryOnlyAuthentication -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName AzureADOnlyAuthentication
----------------- ---------- ----------- -------- -----------
ResourceGroup01   Server01   True
```

<span data-ttu-id="3cfa1-112">Det här kommandot får Azure Active Directory (Azure AD) autentiseringskrav endast för en AzureSQL-server som heter Server01 som är kopplad till en resurs grupp med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-112">This command gets Azure Active Directory (Azure AD) only authentication requirement for an AzureSQL server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3cfa1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3cfa1-113">PARAMETERS</span></span>

### <span data-ttu-id="3cfa1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfa1-114">-DefaultProfile</span></span>
<span data-ttu-id="3cfa1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cfa1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cfa1-116">-InputObject</span></span>
<span data-ttu-id="3cfa1-117">SQL Server-objekt som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-117">The SQL server object to use.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: UseInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cfa1-118">-ResourceGroupName</span></span>
<span data-ttu-id="3cfa1-119">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cfa1-120">-ResourceId</span></span>
<span data-ttu-id="3cfa1-121">ID för den instans som ska användas</span><span class="sxs-lookup"><span data-stu-id="3cfa1-121">The resource id of instance to use</span></span>

```yaml
Type: System.String
Parameter Sets: UserResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa1-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3cfa1-122">-ServerName</span></span>
<span data-ttu-id="3cfa1-123">Namnet på Azure SQL Server-verifiera Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-123">The name of the Azure SQL Server the Azure Active Directory only authentication is in.</span></span>

```yaml
Type: System.String
Parameter Sets: UseResourceGroupAndServerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfa1-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3cfa1-124">-Confirm</span></span>
<span data-ttu-id="3cfa1-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cfa1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cfa1-126">-WhatIf</span></span>
<span data-ttu-id="3cfa1-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cfa1-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cfa1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfa1-129">CommonParameters</span></span>
<span data-ttu-id="3cfa1-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cfa1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfa1-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cfa1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfa1-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3cfa1-132">INPUTS</span></span>

### <span data-ttu-id="3cfa1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3cfa1-133">System.String</span></span>

## <span data-ttu-id="3cfa1-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3cfa1-134">OUTPUTS</span></span>

### <span data-ttu-id="3cfa1-135">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span><span class="sxs-lookup"><span data-stu-id="3cfa1-135">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryOnlyAuthenticationModel</span></span>

## <span data-ttu-id="3cfa1-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3cfa1-136">NOTES</span></span>

## <span data-ttu-id="3cfa1-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3cfa1-137">RELATED LINKS</span></span>

[<span data-ttu-id="3cfa1-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3cfa1-138">Enable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Enable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3cfa1-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span><span class="sxs-lookup"><span data-stu-id="3cfa1-139">Disable-AzSqlServerActiveDirectoryOnlyAuthentication</span></span>](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[<span data-ttu-id="3cfa1-140">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3cfa1-140">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3cfa1-141">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="3cfa1-141">Get-AzSqlServerActiveDirectoryAdministrator</span></span>](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="3cfa1-142">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="3cfa1-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)