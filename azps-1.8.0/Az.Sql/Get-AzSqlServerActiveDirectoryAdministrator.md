---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FEDA14CF-632F-4D15-A22B-C73A1298094F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: f98e362c10a0773f16ae4b687e5d725fb12f5053
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746683"
---
# <span data-ttu-id="28c2b-101">Get-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="28c2b-101">Get-AzSqlServerActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="28c2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="28c2b-103">Hämtar information om en Azure AD-administratör för SQL Server.</span><span class="sxs-lookup"><span data-stu-id="28c2b-103">Gets information about an Azure AD administrator for SQL Server.</span></span>

## <span data-ttu-id="28c2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28c2b-104">SYNTAX</span></span>

```
Get-AzSqlServerActiveDirectoryAdministrator [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28c2b-105">DESCRIPTION</span></span>
<span data-ttu-id="28c2b-106">Cmdleten **Get-AzSqlServerActiveDirectoryAdministrator** hämtar information om en Azure Active Directory (Azure AD-administratör) för en AzureSQL-server i det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="28c2b-106">The **Get-AzSqlServerActiveDirectoryAdministrator** cmdlet gets information about an Azure Active Directory (Azure AD) administrator for an AzureSQL Server in the current subscription.</span></span>

## <span data-ttu-id="28c2b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28c2b-107">EXAMPLES</span></span>

### <span data-ttu-id="28c2b-108">Exempel 1: hämtar information om en administratör för en server</span><span class="sxs-lookup"><span data-stu-id="28c2b-108">Example 1: Gets information about an administrator for a server</span></span>
```
PS C:\>Get-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

<span data-ttu-id="28c2b-109">Med det här kommandot får du information om en Azure AD-administratör för en server med namnet Server01 som är kopplad till en resurs grupp med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="28c2b-109">This command gets information about an Azure AD administrator for a server named Server01 that is associated with a resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="28c2b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28c2b-110">PARAMETERS</span></span>

### <span data-ttu-id="28c2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c2b-111">-DefaultProfile</span></span>
<span data-ttu-id="28c2b-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="28c2b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28c2b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c2b-113">-ResourceGroupName</span></span>
<span data-ttu-id="28c2b-114">Anger namnet på den resurs grupp som SQL-servern har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="28c2b-114">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="28c2b-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28c2b-115">-ServerName</span></span>
<span data-ttu-id="28c2b-116">Anger namnet på den SQL Server som den här cmdleten får information om.</span><span class="sxs-lookup"><span data-stu-id="28c2b-116">Specifies the name of the SQL Server for which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28c2b-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28c2b-117">-Confirm</span></span>
<span data-ttu-id="28c2b-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28c2b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c2b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c2b-119">-WhatIf</span></span>
<span data-ttu-id="28c2b-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28c2b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c2b-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28c2b-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c2b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c2b-122">CommonParameters</span></span>
<span data-ttu-id="28c2b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c2b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c2b-124">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28c2b-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c2b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28c2b-125">INPUTS</span></span>

### <span data-ttu-id="28c2b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="28c2b-126">System.String</span></span>

## <span data-ttu-id="28c2b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28c2b-127">OUTPUTS</span></span>

### <span data-ttu-id="28c2b-128">Microsoft. Azure. commands. SQL. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel</span><span class="sxs-lookup"><span data-stu-id="28c2b-128">Microsoft.Azure.Commands.Sql.ServerActiveDirectoryAdministrator.Model.AzureSqlServerActiveDirectoryAdministratorModel</span></span>

## <span data-ttu-id="28c2b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28c2b-129">NOTES</span></span>

## <span data-ttu-id="28c2b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28c2b-130">RELATED LINKS</span></span>

[<span data-ttu-id="28c2b-131">Remove-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="28c2b-131">Remove-AzSqlServerActiveDirectoryAdministrator</span></span>](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="28c2b-132">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="28c2b-132">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](./Set-AzSqlServerActiveDirectoryAdministrator.md)

[<span data-ttu-id="28c2b-133">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="28c2b-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

